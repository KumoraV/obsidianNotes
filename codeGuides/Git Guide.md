~~~How To Use Git~~~
1) Intialize the folder you are working on 
	- If the folder you are in is not already in git, initalize it
2) Make a branch if needed
3) Track the files by adding them to the staging area
	- The staging area is where you add files that are ready
	to be commited, or ready to be sent.
4) Commit your changes
	- This will commit all the files in the staging area
~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~~Start Guide~~~~~
Set username - $ git config --global user.name "yourUsername"
Set email - $ git config --global user.email yourEmail@mail.com
Initalize repository (while in dir) - $ git init
Check status of repo - $ git status

Track file - $ git add fileName.txt
Untrack file - $ git rm --cached fileName.txt
Track all files - $ git add --all
OR $ git add .
OR $ git add -A

Commit - $ git commit -m "commit message - write here"

Check differences and changes - $ git diff
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

~~~~GitHub~~~~~
Push
	This will save your local dir onto github's cloud. 
	First make a new repo in github, and then following the instructions to push an exsisting repo.
Push all branches
	$ git push --all

Pull Request
	Pull is when you merge a branch into the main branch.
	You do this by submitting a pull request in github.
	And then by accepting the pull and merging the branches.

Pull
	This is when you get the cloud repo into your local machine.
	To do this, go to dir you want to save it to and then
	1) $ git fetch
	2) $ git merge
	OR
	$ git pull

Clone
	This will make a copy of the repo onto your local machine
		$ git clone "repoURL.com"
~~~~~~~~~~~~~~~~

~~~~~Branches~~~~~~
Make branch
	$ git branch branchName
View branches
	$ git branch
		Current branch has * next to it
Change branch
	$ git switch branchName
	$ git switch -c branchName
		This will make the branch and switch to it
Merge branch
	$ git merge -m "Merge message write" branchName
		The branch name you put in will be merged into your 
		current branch.
		So you should be in master branch, and then type
		the branch in which you worked on
Delete Branch
	$ git branch -d branchName
Merge Conflict
	This happens when the same file is edited on two different branches,
	and then you try to merge them together.
	When this happens, a new branch is made. The file will have two sections.
		 HEAD has the master file edits and the 
		 other section will have the other branche's edits.
	In the file, delete the section you don't want and then commit to fix the conflict.
~~~~~~~~~~~~~~~~~~

~~~~~~~
How to ingnore files in git
	Go into dir and make a file called ".gitignore"
	It should be saved as a git ignore source file
	In the file, write the files you want to be ignored
Commit without staging
	$ git commit -a -m "Commit message here"
Restore deleted file
	$ git restore "fileName.txt"
View commit history
	$ git log
	Summarize - $ git log --oneline
	See all changed - $ git log -p
		Press q to quit

