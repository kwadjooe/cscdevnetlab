Basic Git Workflows
Talk to us

When you set out to accomplish a task that you have completed before, whether you are aware of it or not, you have workflows that you follow for the task. Developers (which now includes you) are the same. When they complete a task, they have workflows that they follow. While these workflows may be new to you, they will quickly become your own.

Cloning a repository

When you want to work with someone else's code, you first have to get it on your machine. For this task, use the git clone command.

When you clone a repository, you copy files to a folder in the location where you run the command.

Use the following command to clone the correct sample code repository:


git clone --branch main https://github.com/CiscoDevNet/dne-devfun-code.git
This example shows the resulting output in your terminal window:

developer:src > git clone --branch main https://github.com/CiscoDevNet/dne-devfun-code.git
Cloning into 'dne-devfun-code'...
remote: Enumerating objects: 1310, done.
remote: Counting objects: 100% (1310/1310), done.
remote: Compressing objects: 100% (1083/1083), done.
remote: Total 1310 (delta 187), reused 1306 (delta 183), pack-reused 0
Receiving objects: 100% (1310/1310), 3.30 MiB | 1.51 MiB/s, done.
Resolving deltas: 100% (187/187), done.
When you run this command, the Git client connects to the URL provided and clones a full copy of the repository to the system. By the way, when we say "clone," we mean it. When you clone a repo, you are indeed getting a complete copy of the repository and all its contents. From the first commit to the last, git clone copies locally to your computer all of the files that have ever been committed to the repository.

Tip: To see the cloned repos in the in-browser file system, click the refresh icon until you see the directory.
In-browser file refresh

Now that you have our repo on your computer, let's get it ready for you to edit and commit your changes. Change to the cloned repository:


cd dne-devfun-code
From the repo root, you can see all the changes that were made in the history of the repo. Let's give it a try.


git log
If you use git log in a repo with many commits, press the spacebar to page through the commits and q to quit.


q
If you are not in the correct directory, one that does not contain files from a Git repository, you can get this error on any git command:
fatal: not a git repository (or any of the parent directories): .git

If this error message appears, change directories to your repository, such as cd dne-dna-code. Let's carry on.
