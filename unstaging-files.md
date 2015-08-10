# Unstaging a file

1. Be sure to be in a clean state by typing git status. If Git says "nothing to commit, working directory clean," we are ready to start.
2. Create a new file touch NewFile.txt.
3. Using git status again, verify that NewFile.txt is untracked.
4. Add it to the index so that Git can start tracking it. So, use the git add NewFile.txt command and go on.
5. When done, use git reset HEAD <file> command to back the file in the untracked status.

Another way to unstage a file that you just added is to use the git rm command.
If you want to preserve the file on your folder, you can use the --cached option. 
This option simply removes it from the index, but not from the filesystem. 
However, remember that git rm is to remove files from the index. 
So, if you use the git rm command on an already committed file, you actually mark it for deletion. 
The next commit will delete it.