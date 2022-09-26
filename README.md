# bspwm

Bspwm is a tiling window manager that represents windows as the leaves of a full binary tree.

## Install the following dependacies

    sudo apt install bspwm polybar rofi sxhkd nitrogen lxappearance lxpolkit
    compton

## Move the folders; bspwm, polybar, rofi sxhkd to ~/.config

## Configure touchpad to allow for greater features, most notably natural scrolling.

### Step 1: install the driver

    sudo pacman -S xf86-input-libinput
    apt search on debian based distros and install the equivalent driver

### Step 2: Edit or create the driver 

    cd /etc/X11/xorg.conf.d/30-touchpad.conf

### Copy and paste the following into that file for natural scrolling and tap-to-click functions.

    Section "InputClass"
        Identifier "devname"
        Driver "libinput"
            Option "Tapping" "on"
            Option "NaturalScrolling" "true"
    EndSection
