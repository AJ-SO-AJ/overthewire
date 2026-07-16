# Level 19 to 20

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.

So ./bandit20-do is a setuid ELF 32-bit executable. It sets your effective user id of the executing process to be bandit20, so we can read bandit20's password.

If we use cat with this privilege we should be able to read /etc/bandit_pass/bandit20
