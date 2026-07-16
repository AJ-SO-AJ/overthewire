# Level 28 to 29
Clone another git repo

README gives some hint

- username: bandit29
- 
- password: xxxxxxxxxx
- 
The idea is that they've done a git commit to fix the info leak. So you need to access a previous git commit.

git log -> gives info of previous commits

git show <commit_id> gives what changed in that commit. One of the previous commits had the password written before they made another commit to hide it.
