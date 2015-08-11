# Misc.:

### Force to previous commit

git reset HEAD --hard or alternatively, use commit hash instead

### Force your local repo. to be exactly the same as a remote one

git reset --hard origin/master 

### Rebasing keeping no fast forward

git rebase -p -i commit_hash: useful when deleting a set of —no-ff commits but without adding a revert commit

### Revert a --no-ff commits with a revert commit

git revert -m 1 commit_hash: 

### Suggested alias for .bash_profile

alias git_graph='git log --graph --decorate --pretty=oneline --abbrev-commit'