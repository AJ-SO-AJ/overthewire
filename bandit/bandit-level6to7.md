# Level 6 -> 7
You can use find to find a file that is owned by user and group, and also how big it is.

find -type f (file) -user bandit7 (User ownership) -group bandit6 (Group ownership) -size 33c

find / -type f -user bandit7 -group bandit6 -size 33c

Can also add 2>/dev/null (to get rid of error messages)
