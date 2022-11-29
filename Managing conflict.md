Managing Merge Conflicts
Talk to us

At some point, you're going to have a merge conflict. Conflicts arise when users have made overlapping changes to a file, and Git can't automatically merge the changes.

In this exercise, you will deliberately create a merge conflict and resolve it.

Creating a merge conflict

Note: This exercise has you commit a change directly to main. This is generally not considered Git best practice, and is only being done to demonstrate the process for resolving conflicts.
Create a file called DEVNET.txt.


cd /home/developer/src/devnet-devfun/
echo "I'm a git genius now!" >> DEVNET.txt
In the file browser, open DEVNET.txt and confirm the content. Now commit the change.


git add DEVNET.txt
git commit -a -m "Created DEVNET.txt"
Create a new branch named test and switch to it.


git branch test
git checkout test
In the text editor, make a change to DEVNET.txt and replace genius in I'm a git genius now! with beginner. This time, try using the sed command.


sed -i 's/genius/beginner/' DEVNET.txt
Refresh the file list, open DEVNET.txt, and confirm the change.

Commit your change.


git add DEVNET.txt
git commit -a -m 'changed genius to beginner'
Switch back to the main branch.


git checkout main
Make a change to the same line by modifying genius in I'm a git genius now! to wizard this time and commit your change.


sed -i 's/genius/wizard/' DEVNET.txt
git commit -a -m 'changed genius to wizard'
Try to merge main and test with git merge test:


git merge test
You should see a message similar to the following example:

Auto-merging DEVNET.txt
CONFLICT (content): Merge conflict in DEVNET.txt
Automatic merge failed; fix conflicts and then commit the result.
Resolving the conflict

Refresh the file list and click on DEVNET.txt to open it in the file browser. You should see some new text in your file.

<<<<<<< HEAD
I am a git beginner now!
=======
I am a git wizard now!
>>>>>>> test
This shows you where the HEAD version (main in this example) conflicts with the test branch version.

You have to fix this manually. Often, you will use a merge tool, but for this example, you can use the text editor.

Navigate through the lines of text in the DEVNET.txt file and delete the following lines. Leave the line I am a git wizard now! intact.

<<<<<<< HEAD
I am a git beginner now!
=======
>>>>>>> test
Commit the change.


git commit -a -m 'manually merged from branch test'
Git can now commit the file changes successfully, saving only the version that you want to keep.
