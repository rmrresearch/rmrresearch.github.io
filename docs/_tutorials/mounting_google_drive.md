---
title: Mounting Google Drive on Ubuntu
---

As of the time of writing, Google Drive has mount support for Windows and 
MacOS, but not Linux. 

# Obtain rclone

We're going to use a program called `rclone` to mount Google Drive. On
Ubuntu you can obtain it via:

```.sh
sudo apt-get install rclone
```

Once you have rclone

# Mouting Google Drive
Make a directory.

```.sh
rclone mount --daemon --vfs-cache-mode writes "<remote>": "<local/path>"
```

Replacing `<remote>` with the value you entered in the previous

# Acknowledgements

I pieced this solution together from the following sources:

[rclone hints](https://askubuntu.com/a/1332056)