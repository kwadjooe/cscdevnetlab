Preparing the Repo for Your Changes
Talk to us

When you first clone a repository, you see the default branch for a repository, which is usually called main.

Note: If you have not run the command git config --global init.defaultBranch main, your default branch may be called master. Use the configuration command to change the default branch.
You can verify which branch you are working on and the status of your working tree with the git status command:

Run this command in the terminal:


git status
Git returns the following response:

On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
If you start editing files on the main branch and committing your changes, your local repository immediately goes out of sync with the remote server. That might not be a problem, but someone else can commit changes to the main branch and push their changes to the server before you push yours.

In that case, you have to merge, or reconcile, their changes with your own before you push your changes to the server. You cannot even pull updates from the server on the main branch until you reconcile the discrepancy.

"Wait," you say, "I thought this whole version control thing makes collaborating on files easier." It does, but you must create a branch.

Run this command in the terminal to create a new branch called mycode:


git checkout -b mycode
Git returns the following response:

Switched to a new branch 'mycode'
Use the git checkout command to switch between branches. Adding the -b option instructs Git to create a new branch and then switch to it.

When you create a branch on your local repository, you are creating a safe place to edit files in the repo. Any changes that you make and commit are local to this new branch. You aren't making any commits to the branches that are synced with the remote server, so you can always pull down local copies of updates that other developers make to branches on the remote server.

Run the git branch command at any time to see which branches you have locally. The asterisk * indicates which branch is active:


git branch
 Click for Expected Output
 
 
 Keeping Your Local Repository Up-to-date
Talk to us

Over time, your local Git repository will get out of sync with the remote repository. As developers push commits to the server, you need to download these updates to your local repository. If you have been making your changes to your own local branch (which is the best practice), you can update your local repo with the updates from the remote repo with the git fetch command.

Note: If you recently cloned your repo, the remote may not have updates for you to retrieve.
To download the latest updates, run the following command in the terminal:


git fetch
 Sample Output
You have cloned our repository, created a local branch for your edits, and know how to keep your local repo in sync with our remote. You are ready to make and commit your changes.