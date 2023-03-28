---
title: Mounting Google Drive on Ubuntu
---

As of the time of writing, Google Drive has mount support for Windows 
and MacOS, but not Linux. After struggling to find a mechanism for
mounting Google Drive on Ubuntu I stumbled on the following solution.

# Obtain rclone

We're going to use a program called `rclone` to mount Google Drive. On
Ubuntu you can obtain it via:

```.sh
sudo apt-get install rclone
```

# Configure Google Drive Mount

Once you have rclone you need to configure it for you system. 
Unfortunately, this requires answering a series of somewhat cryptic
questions. Thankfully, you only have to do this once.

To start the configure run:

```.sh
rclone config
```

You should be presented with the following questions. For your 
convenience we have also recorded our answers to the questions.

1. No remotes found, make a new one?
   - Answer: n
2. name> 
   - Answer: remote
   - Referred to as `$remote` in the next section.
3. Type of storage to continue.
   - Answer: drive
   - As of the time of this writing "drive" is the key for Google Drive.
     If that changes, use the key for Google Drive.
4. Google Application Client Id
   - Answer: Leave blank
5. Google Application Client Secret
    - Answer: Leave blank
6. Scope that rclone should use when requesting access from drive.
    - Answer: 1
7. Service Account Credentials JSON file path
    - Answer: Leave blank
8. Remote config
    - Answer: y
9. Configure this as a Shared Drive (Team Drive)?
    - Answer: n
10. (At this point it should print out the configuration)
    - Answer: y

If that was successful it's time for the final step...

# Mouting Google Drive

If you have not done so before, create an empty directory where you
want your Google Drive mounted. If for example you want your drive
mounted at `/home/ryan/GoogleDrive` ensure that an empty directory
called `GoogleDrive` exists in `/home/ryan`. Wherever you decide to
put Google Drive, we'll call that spot `$mount`.

In terms of the `$remote` you specified during the config, and `$mount`
which we just defined the actual command for mounting Google Drive is:

```.sh
rclone mount --daemon --vfs-cache-mode writes "$remote": "$mount"
```

This will spawan a daemon to mount Google Drive, which will remain 
active until you stop it.

# Using the Mount

At this point, you should be able to use your Google Drive just like
any other directory on your local file system. In particular it
should appear as a valid path when you attempt to open or save files
from within another program.

# Acknowledgements

I pieced this solution together from the following sources:

[solution overview](https://askubuntu.com/a/1332056)
[rclone config](https://rclone.org/drive/)