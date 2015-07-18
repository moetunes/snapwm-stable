##snapwm-stable
### it's minimal and dynamic

I started this from catwm 31/12/10 ( https://bbs.archlinux.org/viewtopic.php?id=100215&p=1 )
    See snapwm.c for thanks and licensing.
Screenshots and ramblings/updates at https://bbs.archlinux.org/viewtopic.php?id=126463


###Summary
-------


**snapwm** is a xinerama aware, minimal and lightweight dynamic tiling window manager.

All configuration is read from three files in ~/.config/snapwm/ . There
 are well commented samples of each file to assit in initial setting up.

*rc.conf* has colours and window manager configurations.

*key.conf* is mandatory for shortcuts and commands to run.

*apps.conf* is optional and where apps settings are read from.


###Development
------------

Enhancements and bugfixes are developed and tested in the Nextwm
 repository first.


###Modes
-----

It allows the "normal" method of tiling window managers with the new
    window as the master or with the new window opened at the bottom
    or the top of the stack.

 *There's vertical tiling mode:*

    --------------
    |        | W |
    |        |___|
    | Master |   |
    |        |___|
    |        |   |
    --------------

 *Horizontal tiling mode:*

    -------------
    |           |
    |  Master   |
    |-----------|
    | W |   |   |
    -------------

 *Grid tiling mode:*

    -------------
    |      | W  |
    |Master|    |
    |------|----|
    |      |    |
    -------------

 *Stacking mode:*

    -------------
    |   _______  |
    |  |  ___  | |
    |  | |___| | |
    |  |_______| |
    -------------


 *Fullscreen mode*(which you'll know when you see it)

 All accessible with keyboard shortcuts defined in key.conf file.
 
 * The window *W* at the top of the stack can be resized on a per desktop basis.
 * Changing a tiling mode or window size on one desktop doesn't affect the other desktops.
 * Windows can be added/removed to/from the master area with keyboard shortcuts
 * There is a bar with a desktop switcher, space to show the focused window's name and space to show external text.
 * The rc files are reloadable 'on the run'.


###Installation
------------

Need Xlib, Xinerama and Xrandr, then:

    Copy the sample.rc.conf file to $HOME/.config/snapwm/rc.conf and edit it to suit.

    Copy the sample.apps.conf file to $HOME/.config/snapwm/apps.conf and edit it to suit.

    Copy the sample.key.conf file to $HOME/.config/snapwm/key.conf and edit it to suit.

    $ make
    # make install
    $ make clean


###Output in the Bar
-----
To have the time shown in the bar using bash:

    while true; do sleep 1; line=$(date +%H:%M:%S); xsetroot -name "$line"; done


###Bugs
----

[ * No bugs for the moment ;) (I mean, no importants bugs ;)]

