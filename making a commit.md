Making a Commit
Talk to us

Committing your changes to a repository is a two-step process:

Add: Stage files to the commit with git add.
Commit: Commit the files to the repository with a commit message and git commit.
Try by running the following commands in the terminal:

This command adds the current date to the bottom of the change_me.txt file.


date >> intro-python/git-basics/change_me.txt
Review it to check the change, by listing out the contents of the file in the terminal window:


cat intro-python/git-basics/change_me.txt
Next, you add the file to confirm that Git knows about it and puts it "under" version control:


git add intro-python/git-basics/change_me.txt
Now, commit it to the list of changes you want Git to record, and add a commit message. If you want to type the message in manually, you can use another message within the double quotes. This message is an example.


git commit -m "Git Commit - Adds current Date."
The -m option enables you to write a short commit message right there at the command line. Without the -m option, Git opens your environment's default text editor. Using a text editor lets you enter a more detailed and potentially lengthy commit message.

Note: On many systems, the default text editor is vim. To save and quit a file in vim, press the Escape button and enter :q.
Make it your personal best practice to "commit often." Creating a commit is simple for you and a lightweight task for your computer. Committing often ensures that you capture more of the history of your code. You can go back and view commits and past changes anytime.

When you say to yourself, "Yeah! My code (or some portion of it) is working!" then commit.

Next, let's create a repository that you can play around with, in your own area on GitHub.