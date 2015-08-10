# Misc.:

- git reset --hard origin/master: forcing your local repo. to a remote one
- git rebase -p -i commit_hash: rebasing keeping no fast forward
- git revert -m 1 commit_hash: revert a --no-ff commits with a revert commit

## git_graph:

Suggested alias for .bash_profile:
alias git_graph='git log --graph --decorate --pretty=oneline --abbrev-commit'