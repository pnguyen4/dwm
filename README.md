dwm - dynamic window manager
============================
dwm is an extremely fast, small, and dynamic window manager for X.

Version git-20180502-c8e9479

Applied (official) patches
-------------------------
The following patches have been applied manually

1. Systray:
    - dwm-systray-20180314-3bd8466.diff

2. Tab Mode:
    - dwm-tab-v2b-pertab-56a31dc.diff

3. Pertab:
    - see above (combined patch)

4. Resize Corners
    - dwm-resizecorners-6.1.diff

5. EWMHtags
    - dwm-ewmhtags-20180101-db22360.diff

6. Xtile
    - dwm-6.0-xtile.diff

7. Scratchpad
    - dwm-scratchpad-20170207-bb3bd6f.diff

8. Scheme Switch
    - dwm-scheme_switch-20170804-ceac8c9.diff


Personal Additions
------------------
- Default font is terminus at 10pt
- modified config.mk for OpenBSD
- mod key set to super ('windows') key
- resizehints disabled
- Manpage edited to include xtile commands 


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

If you are going to use the default bluegray color scheme it is highly
recommended to also install the bluegray files shipped in the dextra package.


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
