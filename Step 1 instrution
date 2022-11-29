Configuring Git Locally
Talk to us

When you make a commit to a Git repository, Git automatically includes (in the indelibly hashed and stored commit) the name and e-mail address of the person that made the commit and a non-optional commit "message." When done right (which as you would expect doesn't happen all the time), commit messages can serve as descriptive change logs that record the history of the changes in the project.

Telling Git to default to "main" branch

Now that GitHub defaults to using the main branch on all new repositories created, you want to set up your local Git so that when you type git init the branch created is also named main.


git config --global init.defaultBranch main
Telling Git who you are (one-time setup)

You need to tell Git who you are before you can commit any changes to a repository.

Run the following git config commands in the terminal. Use your own name and the e-mail address that you used when you created your GitHub account:

git config --global user.name "Your Name"
git config --global user.email your@email-address.com
If you ever see any errors about permissions from Git, make sure you have correctly set your user.name and user.email. You can always look at those settings by running this command to see the current configuration:


git config --list
Do you see your name and email address in the output? Look for rows like these:

user.name=Cisco Cisconian
user.email=cisconian@cisco.com
Do you have a row that has init.defaultbranch=main?

Great, then you are all set. Carry on.

Create a personal access token

When you interact with github.com, you need a personal access token. Use the token like a password, and treat it with the same level of security. When a token expires, you must create a new one.

Create a personal access token with repo permissions in the Settings of your personal GitHub account, under Personal access tokens. Refer to GitHub's documentation for "Creating a personal access token".

In these exercises, enter the token whenever you're prompted for a password, as shown in the following example.

developer:src > git clone https://github.com/username/repo.git
Username: your_username
Password: your_token