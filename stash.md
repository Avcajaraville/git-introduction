# Stash

## The problem:

You are working on your local repository. Suddenly you have to switch to another branch, but you dont want to commit (because reasons: maybe its incomplete, maybe you dont want to polute your commit historic, ...)

## The solution:

git stash !

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. Modify some of the files on the repo.
3. Do a git stash
4. Switch branch
5. To recover your changes, once you are in the correct branch, do a a git stash apply
