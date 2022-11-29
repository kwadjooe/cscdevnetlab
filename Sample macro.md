A Sample Code Workflow
Talk to us

Because you know some of the basic Git workflows, you have already learned a macro workflow. This workflow provides a consistent process to complete larger portions of work.

Memorize Git Commands

Image Source: xkcd.com

You now have a workflow whenever you perform the following tasks:

Download (clone) a local copy of a remote repository to your workstation.
Create a "safe place" (branch) for you to make edits.
Save (commit) your incremental changes.
Git Sample-Code Workflow

This macro workflow follows these steps:

Step	Action	Git Commands
1	Clone the Remote Repository	git clone <url>
2	Create and Checkout a Local Branch	git checkout -b <new branch name>
3	Incrementally Commit Changes	git add <new or modified file>
git commit -m "Commit Message"