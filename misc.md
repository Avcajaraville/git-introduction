# Misc.:

### Force to previous commit

git reset HEAD --hard or alternatively, use commit hash instead

### Force your local repo. to be exactly the same as a remote one

git reset --hard origin/master

### Reverting a file to the state that had on the last commit

git checout file_name

### Rebasing keeping no fast forward

git rebase -p -i commit_hash: useful when deleting a set of —no-ff commits but without adding a revert commit

### Revert a --no-ff commits with a revert commit

git revert -m 1 commit_hash: 

### Suggested alias for .bash_profile

alias git_graph='git log --graph --decorate --pretty=oneline --abbrev-commit'

### Diff by highlighting inline word changes instead of whole lines

git diff file_name --word-diff