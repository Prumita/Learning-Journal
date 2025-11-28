Linux is good for performance, it is open source, and Walmart use it!

Linux is case sensitive.

Lots of commands for Linux, everything starts at /root.

/bin means binary executibles.

/sbin is system executibles.

Other mount points are /media or /mnt. Directory that allows you to access additional files. So you can think you might put a usb in, then say where that usb is accessible, specify a directory for it. But not just physiucal things like that, could be shared drives etc as well.


/dev is devices including hard drives. So if we're assuming the hard drive is internal then it's d, but if it's additional then mnt or media.

### Logging in
Virtual console that's text based, or there's the graphical login which is a display manager.

In linux a shell is like command prompt. It's a command line interpreter (CLI), it acts as an interface between the user and the operating system's kernel.

Root is all powerful so you should never leave that account open, need to use user credentials and access based and role based permissions.
so root is a superuser as well as the core of everything.
Normal user accounts don't need to be able to write anything to the root. 
Traditional DAC security transactions, your read only, read write etc.
So in linux chat we've got

r-- is read only
rw- is read, write and execute for members of the group owning the file
rwx is read, write and execute for owner of the file.
- means a file, d means a directory

use chmod to amend the permissions on the file.

|Command|Description|
|----------|-----------|
|cd, change directory | cd .., cd -, cd ~ /mydir, cd /home/usman, cd|
|su| Swtich user, su - (complete user environment)|
| passwd| change password|
|ps, process information| process information: ps, ps aux, pstree, psfax, top|
|free, memory information | Free -m|
|Cal, calendar information | cal, cal 2009|
|cat, concatenate /display files| cat/home/usman/myfile|
|clear| clears the screen|
|date, see/modify system data & time|date, date [MMDDhhmm[[CC]YY][.ss]]|
|df, disc space usage| df-h|
|du, file space usage|Du - sh|
|uname, print system info| uname [-a, -s, -n, -r, -v, -m]|

cd is used for changing directories.
cd.. goes back up a directory
cd- shortcut for $OLDPWD, which would let you go back to previous working directory
cd take you to your home directory.

su switch user

--help or -h to get help.

rm - r would remove a directory containing all of the files.


