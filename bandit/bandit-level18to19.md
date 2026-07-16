# Level 18 -> 19

You connect using password but it logs you out because .bashrc is set that way.

You can use ssh to run commands before you even fully get logged in / before .bashrc is read (non-interactive execution).

ssh user@host command -> will run the command

