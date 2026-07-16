# Level 32 to 33

We were logged in some UPPER CASE SHELL

It converts all your input to upper case. It also doesn't allow you to execute anything. The trick is that you can type one thing, $0.

$0 is a variable for shell. It holds the name of the current shell. If you execute $0, it will open that shell.

Using that to our advantage, I opened bash. I was logged in bandit33. That allows us to cat the /etc/bandit_pass/bandit33 since we have access.
