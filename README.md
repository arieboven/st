# st - simple terminal | my custom build
[st](https://st.suckless.org/) is a simple terminal emulator for X which sucks less.

In this build I have added some patches for more features, these patches can be found on the [suckless.org](https://st.suckless.org/patches/) website. The patches that I added:  
| | |
| :---: | :---: |
| anysize | scrollback |
| blinking_cursor | scrollback-mouse-altscreen |
| externalpipe | vertcenter |
| focus | w3m |
| font2 | xresources |
---

## Features
+ Scrollback with `Alt + j/k`, `Alt + u/d`, `Shift + pageUp/pageDown` or with mousewheel (no shift)
+ Incr/decr fontsize with `Alt + ./,`
+ Different focus transparency, witch values can be given by arguments `-A` for focused and `-U` for unfocuesed with values between 0-1. default value can be set in the config file
+ Load xresources colors in configuration st
+ Copy/open urls with `st-urlhandler` and copy output form terminal with `st-copyoutput`, whitch I have from the build of [Luke Smith](https://github.com/LukeSmithxyz/st)
---

## Requirements
In order to build st you need the Xlib header files.  
**!!! For colored text or emojis install [libxft-bgra](https://aur.archlinux.org/packages/libxft-bgra/)**, if not st might crash when viewing emojis.  
For `st-urlhandler` and `st-copyoutput` *dmenu* is required.

---
## Installation
Edit config.mk to match your local setup (st is installed into
the /usr/local namespace by default).

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install
---

## Credits
Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.


