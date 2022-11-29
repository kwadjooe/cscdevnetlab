Changing files
Talk to us

If you change a file under Git's version control, Git knows.

Let's practice changing files with the in-browser editor.

Look at the intro-python/git-basics/change_me.txt file:


cat intro-python/git-basics/change_me.txt
It's a one-liner right now:

If you change even one character in this file... Git will know.
Open the intro-python/git-basics/change_me.txt file in the in-browser editor and add, edit, or delete anything that you like.



Then run the following command in the terminal:


git status
 Expected Output

git diff
 Sample Output
From the git status output, you can see that Git detected the modification to the change_me.txt file, and from the git diff output you can even see what changed in the file. In my example, I added "Here's more than one character." to the end of the file.

Reverting changes

Sometimes you make changes and then decide that you want to return to a past commit. Here are the simple workflows that can help you back out changes.

Restore the last committed version

After you change a file, but before you commit it, you decide to revert those changes and restore the last committed version of the file back. Use git checkout to retrieve the last version of the file, overwrite the changes that you have made, and restore the file to its last committed version.


git checkout intro-python/git-basics/change_me.txt
Expected output:

Updated 1 path from the index
You can now run git status to see that the change you made previously is no longer there and not tracked by Git.


git status
Expected output:

On branch mycode
nothing to commit, working tree clean
It's like nothing ever happened here. You can revert changes to a single file with the git checkout </path/to/file.name> command. What about lots of changes in several files?

Revert multiple changes

After you change several files, you want to revert all those changes and restore the "last known good state": the last commit. Use git reset to restore your working directory to the last commit.

Note: You will lose all the changes that you have made since your last commit.
git reset --hard
Delete a branch

After you create a branch to experiment with some changes, you decide that you want to discard the whole thing. Use git branch --delete to delete the branch.

git branch --delete --force <branch name>
Note: Always be careful when you see options like --hard or --force. When you use these keywords, pause and think about what you are doing, because you lose some work when you run these commands. If that is your intention, proceed. Otherwise, think twice (or three times) before running these commands.
Committing your changes

While the change we made to a trivial text file is, well, trivial, later you will edit code to make it functional. When you get your code working (insert awesome feeling of accomplishment), you are going to want to save that accomplishment and lock it away indelibly in the repository. To save the changes, you will "commit" your changes to the repository in the next step.
