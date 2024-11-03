dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.

Patches
-------
- alwayscenter-20200625-f04cac6
- alpha-20230401-348f655
- smartborders-6.2
- tilegap-6.4
- pertag-20200914-61bb8b2
- focusonclick-20200110-61bb8b2
- ewmhtags-6.2
- focusonnetactive-6.2
- resizecorners-6.5
- cursorwarp-6.3
- actualfullscreen-20211013-cb3f58a
- statuscmd-20210405-67d76bd

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
