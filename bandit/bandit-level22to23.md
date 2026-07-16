# Level 22 -> 23
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

The script runs some myname = user, then creates a mytarget m5dsum from the string "I am user $myname" into cut -d ' ' -f 1. Then it writes the password from bandit23 into a temporary /tmp/$mytarget

If we just execute (echo I am user $mytarget | md5sum | cut -d ' ' -f 1) and replace $mytarget with bandit23, we get the target name. Then we can just cat from the file.
