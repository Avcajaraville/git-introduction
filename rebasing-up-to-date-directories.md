# Rebasing

## The problem:

So, you are on dev., you create a feature branch and start working there. At some point, somebody else made some changes into dev. And you want those changes available on your current branch.
Lets see what happen if you just pull.

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. On master, checkout another branch: git checkout -b test
3. Add some changes and commit them.
4. Checkout back to develop and make some changes there and commit them.
5. Now go back to your test branch, pull and do some other changes, then commit them.
6. Now, back to develop. Merge that branch and do git_graph. Thats pretty disgusting, uh ?

## The solution:

Use git rebase on your feature branch to have all new changes.

1. Repeat steps 1-4.
2. Now, on your feature branch, instead of pulling, do git rebase master.
3. Keep working on your feature branch. Do some commits.
4. Now, back to develop. Merge that branch and do git_graph. Thats much better eh ?