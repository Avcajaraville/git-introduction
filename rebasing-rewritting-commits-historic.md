# Rebasing

## The problem:

You want to rewrite your historic of commits. Reasons may vary, but mostly is about squashing, renaming commits.

## The solution:

Use git rebase -i (interactive mode)

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. Do some dummy commits.
3. Do a git rebase -i commit_rebase and see the options you have there