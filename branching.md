# Branching

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. Create a new branch: git checkout -b test
3. Create a new file: touch test.tmp
4. Add & commit this new file

## Merging: fast-forward
1. Checkout the branch you want to use as a base, in this case, master: git checkout master
2. Merge the feature branch: git merge test
3. The branch is now successfully merged
4. Do git_graph and check the tree

## Merging: non fast-forward
### Reverting previous merge
1. Do a git log in order to see the commits history
2. Select the commit hash corresponding to the state we want to revert
3. Do: git reset COMMIT_HASH —hard (because we want also the file content reverted, in this case, deleted)
4. Now you have reverted your changes
## Merging: non fast-forward
5. Merge now with no fast-forward options: git merge test —no-ff
6. Do git_graph and check the tree (note the main differences between fast forward and no fast forward

## Merging with conflicts

**We just did some merging without any conflicts. Lets see how we will proceed with conflicts:**

1. Lets delete our test branch: git branch -D test
2. Lets revert to a previous state before the merging (you should know how to do this by now)

**We should be now on a clean state**

1. On branch master, checkout a new test branch
2. On test branch, modify the file tmp-files/riders.txt on an arbitrary way (ie: change some lines only). Commit the changes.*
3. Checkout master and modify the same file on an arbitrary way (but not the lines you already changed on step 2). Commit the changes.
4. Merge now (either with ff or not-ff, but I always recommend —no-ff). You will see that there is no conflicts now. This is because the lines affected are not the same on both files. Thus git make an automatic merge and take both modifications (the ones on master & develop).

(\*) On this point, if you merge into master, you wont have conflicts, even when the file has changed. This is because no changes has been done to master, and git assume the latest modifications should be taken. It is an automatically merge.

**Go back to a clean state**

1. On branch master, checkout a new test branch
2. On test branch, modify the file tmp-files/riders.txt on an arbitrary way (ie: change some lines only). Commit the changes.*
3. Checkout master and modify the same file on the same lines you did on step 2. Commit the changes.
4. Merge. You have now conflicts. In order to fix the conflicts, you have to go to the conflicted files.

### Solving conflicts:
Conflicts are marked with: <<<<<<< HEAD, ======= and >>>>>>> branch_name
* Between <<<<<<< HEAD and ======= is what is inside of the current branch. In our case, since we are merging INTO master, this represents master.
* Between  ======= and >>>>>>> branch_name is what is inside of your feature branch.

You have to manually merge this conflicts, add the files once they are resolved, and commit them. I recommend to commit without any parameter, so git will launch your predefined text editor and use some default messages, usually: Merge branch “branch_name”

**Do a git graph and carefully inspect the tree**

Note that master changes are “behind” you branch changes, even when this wasn’t what happened (chronologically speaking). 

