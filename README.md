
I use Hyprland, and this has not been tested on anything else. Probably works for Wayland stuff in general, unsure though.

Also includes a fix for the error:
WARNING: socket file /run/user/1000/swww.socket was not deleted when the previous daemon exited
Error: "Failed to receive answer: io error: Connection reset by peer (os error 104)"

Automatically deletes swww's cache. Also kills and initializes swww.

----------------------------------------------------------
Prerequisites:
- swww
- pywal
- (optional) pywalfox
- (optional) pywalfox firefox extension

- I use zsh and oh-my-zsh, there may be alternatives.
----------------------------------------------------------

Setup Guide

Step 1: git clone this. 

Step 2: Change "$HOME/Downloads/wallpapers/" to the folder/directory you keep your wallpaper images in, OR just rename your wallpapers folder to "wallpapers" and move it to your Downloads folder.

Step 3: (If not using zsh as your shell) Change #!/bin/sh to #!/bin/bash if you are using bash (use echo $0 in the terminal to check which one you're using). Test it with ./newlook while in the folder newlook is located in. If you're using another type, research what to put instead of sh or bash at the end.

Step 4: Make sure to execute this on startup if you want it to change on startup. For hyprland, in your hyprland.conf file, near the top put "exec-once = /home/your-username/path/to/wallpaperchanger" (Downloads by default for me, but I move it to .local/bin/)

If something isn't working, make sure all of the directories are going to the correct area, and that you're executing it on startup correctly.

----------------------------------------------------------

If you use dwm, instead of downloading this:

There is a great video by BugsWriter called "Linux Ricing Crash Course (minimal, simple yet pretty rice for newbies)" where he does this with dwm. 29:24 is around where that part starts, and the complete code is at 33:18. This is basically that but for Hyprland (since as opposed to X11, Wayland is used. I use swww instead of xwallpaper, and had to clear the cache to get it to work).

-----------------------------------------------------------
Credits:
bugswriter (video mentioned above)
pywal
swww
