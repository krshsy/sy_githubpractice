Summary

CHAPTER 5

Distributed Workflows - allows flexibility in how developers collaborate on projects

	Centralized Workflow - single collaboration model; a central hub/repository can accept code where everyone can synchronize their works with
	
		Integration-Manager Workflow - each developer has write access to their own public repository

	Dictator and Lieutenants Workflow - variant of a multiple-repository workflow; used by huge projects (with hundreds of collaborators); eg: Linux kernel
	
The following are commonly used workflows, possible with a distributed system like Git.

As Git is very flexible, people can do work together in many ways
	Contributor count - contribution per users in a day or less
	Workflow in use
	Commit access - workflow required in order to contribute to a project

Private small team - private project with one or two other developers; closed-source

Private managed team - contributor roles are in a larger private group

Forked public project
	$ git clone (url)
	$ cd project
	$ git checkout -b featureA
	# (work)
	$ git commit
	# (work)
	$ git commit
	
Common workflows for dealing with several different type of Git projects

Maintaining a project - accepting and applying patches generated via
	format-patch

	Working in topic branches
		$ git branch sc/ruby_client master
		
	Applying patches from e-mail
		$ git apply /tmp/patch-ruby-client.patch
		
	Checking out remote branches
		$ git remote add jessica git://github.com/jessica/myproject.git
		$ git fetch jessica
		$ git checkout -b rubyclient jessica/ruby-client
		
	Integrating contributed word
		Merging workflows - merges your work into your master branch
		Large merging workflows - master, next and pu
		
	Tagging your releases - dropping a tag on a release can re-create the release at any point going forward
		
	Shortlog
		git shortlog               
	
	
		
