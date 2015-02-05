Summary

CHAPTER 2

	git init 
Is the command used to initialize a repository in an existing directory

It is possible to get a copy of an existing Git repository with the command 
	git clone

Each file in the working directory can be in two states:
	Tracked - files in the last snapshot (unmodified, modified or staged)
	Untracked - any files that were not in the last snapshot and not in the staging area
	
Check status of your files with this command
	git status

Begin tracking new files with the command
	git add

Changing a file that was already tracked is accomplished through staging modified files. It uses the following commands
	git status
	git add
	
Short status flags exists to see changes in a more compact way.

One can ignore files in Github by using the command
	.gitignore
Which will automatically add or ever show you as being untracked

Knowing specific changes in a file can be used through the 
	git diff 
command

After staging the area, you can commit the changes with 
	git commit
	
To remove files from Git, remove it from your tracked files then commit
	git rm
	
Using the
	--cached
option will keep your file in you working tree but will remove it from your staging area

Renaming a file is very much like moving a file (sample snippet below)
	git mv file_from file_to
	
View th commit history with the 
	git log
command

Since log output can take a long time to usually produce, you can use limiting options such as
	--since
	--until

	--amend
option is used for undoing things. Be careful using this since you can't undo some of the undos.

Unstaging a staged file
	git add . 
	git status

Show remote servers you have configured
	git remote
	
Fetching and pulling from remotes
	git fetch
	
Pushing to your remotes
	git push origin master

Inspecting a remote
	git remote show origin

Removing and renaming remotes
	git remote rename
	
Tagging is the ability to tag specific important points

	List your tags
		git tag
	Lightweight tags
		git tag -lw
	Sharing tags
		git push origin v1.5
	Checking out tags
		git checkout -b version2 v2.0.0

Set up an alias for each command
	git config
