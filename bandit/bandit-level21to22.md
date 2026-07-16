# Level 21 -> 22
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

Cron runs scripts periodically. In cron.d, there's a bandit22 cronjob being executed. bandit22 cronjob runs the script bandit22.sh. bandit22.sh has chmod 644 to some /tmp/file, and then writes the bandit_pass/bandit22 into this /tmp/file.

So if we go to cron.d, cat the cronjob we need, cat the script itself, we will see what the script does.

It cats the password to /tmp/t706lds9S0RqQh9aMcz6ShpAoZKF7fgv. I wonder if that is the actual password. Let's see.

No, I just needed to cat that file, but the file is empty and hasn't been modified for 6 days so the cron isn't working properly. I had to see the password online. But the logic is right.
