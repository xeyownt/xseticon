Xterm, and likely many other X11 programs, do not set themselves window icons, which window managers typically use to represent that program window in switcher lists, taskbars, and so on. This program can set the X11 window icon for any given window, to that of a given image file.

Usage
=====
    usage: xseticon [options] path/to/icon.png
    options:
      -name     : apply icon to the window of the name supplied
      -id   : apply icon to the window id supplied
    
    Sets the window icon to the specified .png image. The image is loaded from
    the file at runtime and sent to the X server; thereafter the file does not
    need to exist, and can be deleted/renamed/modified without the X server or
    window manager noticing.
    If no window selection option is specified, the window can be interactively
    selected using the cursor.
    
    Hints:
      xseticon -id "$WINDOWID" path/to/icon.png
    Will set the icon for an xterm.xseticon from Paul Evans (http://www.leonerd.org.uk/).

Build and install instructions
==============================

On Ubuntu:

``` bash
# Install dependencies
sudo apt install libxmu-headers libgd-dev libxmu-dev
# Build
make
# Install
sudo cp xseticon /usr/local/bin
```
On EL7:

```bash
# Install dependencies
sudo yum install libXmu-devel gd gd-devel
# Build
make
# Install
sudo cp xseticon /usr/local/bin
```

Author
======
This is xseticon from Paul Evans (http://www.leonerd.org.uk/).

Note that there is another xseticon from Rustem Valeev on Sourceforge (https://sourceforge.net/projects/xseticon/).

License
=======

See LICENSE file.

