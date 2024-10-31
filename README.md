dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.

Patches
-------
- alwayscenter-20200625-f04cac6
- anybar-polybar-tray-fix-20200810-bb2e722
- fixborders-6.2
- smartborders-6.2
- tilegap-6.4
- pertag-20200914-61bb8b2
- focusonclick-20200110-61bb8b2
- ewmhtags-6.2
- focusonnetactive-6.2

Requirements
------------
In order to build dwm you need the Xlib header files.


Installation
------------
Edit config.mk to match your local setup (dwm is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install dwm (if
necessary as root):

    make clean install


Running dwm
-----------
Add the following line to your .xinitrc to start dwm using startx:

    exec dwm

In order to connect dwm to a specific display, make sure that
the DISPLAY environment variable is set correctly, e.g.:

    DISPLAY=foo.bar:1 exec dwm

(This will start dwm on display :1 of the host foo.bar.)

In order to display status info in the bar, you can do something
like this in your .xinitrc:

    while xsetroot -name "`date` `uptime | sed 's/.*,//'`"
    do
    	sleep 1
    done &
    exec dwm


Configuration
-------------
The configuration of dwm is done by creating a custom config.h
and (re)compiling the source code.
