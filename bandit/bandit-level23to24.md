# Level 23 to 24
A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

NOTE: This level requires you to create your own first shell-script. This is a very big step and you should be proud of yourself when you beat this level!

NOTE 2: Keep in mind that your shell script is removed once executed, so you may want to keep a copy around…

The cron runs a job that executes scripts in /var/spool/$myname/foo if we're logged in as user bandit23, then it deletes the script once executed.

This means there are scripts in /var/spool/bandit24/foo -> we can create a script that will be executed here even if we're not bandit24.

The script we can create is to take bandit24's password and write it in some tmp file:

#!/bin/bash

cat /etc/bandit_pass/bandit24 > /tmp/tmppass24

Then we need to make sure it's executable.

chmod +x [script]
