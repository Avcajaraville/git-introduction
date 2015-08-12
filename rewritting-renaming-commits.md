# Rebasing

## The problem:

You want to rewrite your last commit message or add more files to it

## The solution:

Use git commit --amend

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. Do some commits.
3. Now, if you want to add more files to the last commit, you can do git add files and then git commit --amend. You can also change the commit message.

## The problem:

You want to rewrite an arbitrary commit message or add more files to it

## The solution:

Use git rebase -i (interactive mode). Select the commit BEFORE the point you want to rewrite. 
If you need to add more files, you can git add them and then git commit --amend (and also use the classic rebase options: squash, etc).