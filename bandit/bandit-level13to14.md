# Level 13 to 14
Password is stored in /etc/bandit_pass/bandit14, can be read by user bandit14. You get a private SSH key to log in to the next level.

ssh allows connecting with a private SSH key through the option -i "./fileofkey"

The private SSH key must have these permissions: read & write for user, no permissions for group, no permissions for others. This is bits 600 (4+2 [read&write] for user, 0 for groups, 0 for others) of chmod

chmod 600 ./fileofkey

ssh [host] -l bandit14 -i "./privatekey"

