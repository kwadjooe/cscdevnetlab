Creating a New GitHub repository
Talk to us

In a new tab in your browser, go to https://github.com and log in.

Note: Create a free GitHub account if you have not already and generate a token. Refer to the Prerequisites in the Introduction for more information.
On your GitHub account page, create a new repository in your user space or organization named devnet-devfun. Use these settings:

Name the repo "devnet-devfun":
Create new repo

Keep all the check boxes cleared so that no files are created:
No initial files

Make it a Public repository.
Public repo
Click Create repository.

Click to copy the HTTPS URL, which you will use later.
Copy HTTPS URL

Back in the terminal, navigate to the devnet-devfun directory. If it doesn't already exist, create a folder with the command, mkdir devnet-devfun.


cd /home/developer/src/devnet-devfun
In devnet-devfun, create a README file that contains a title header. For example:


echo "# DevNet Developer Fun Repository README" >> README
Refresh the folder list. You should see the new file in devnet-devfun. If you want, you can open the file in the file editor and add to it.

Initialize the Git repo in devnet-devfun.


git init
Next, add all the files you want to have in the repo, as indicated with the period ..


git add .
Create that commit, or a point in time for the state of the current files in the directory.

The --all or -a parameter tells Git to automatically stage all the files that you have modified (and deleted, although we haven't deleted any with this commit).

The phrase in quotes after the -m parameter is the commit message. You can type in a different one if you want.


git commit --all -m "Adds initial DevNet DevFun project"
Now, make sure you still have the HTTPS URL you copied from the browser:

Copy HTTPS URL

In the terminal window, enter these git commands to add a "remote" named "origin" and then paste in the HTTPS reference, such as https://github.com/justwriteclick/devnet-devfun.git.


git remote add origin <paste the reference>
In the terminal window, set the newly added remote "origin" as the upstream tracker, and push the initial commit to this new branch named main.


git push --set-upstream origin main
Note: Use your authentication token when prompted for a password.
Go to the URL for the repository in GitHub and refresh the page. You should now see your README file in the default main branch. Well done!
