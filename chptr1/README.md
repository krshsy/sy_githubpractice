Summary

CHAPTER 1

Version control - a system that records changes to a file or set of files over time so that you can recall specific versions later

	Local Version Control Systems - uses a simple database that kept all the changes to files under revision control

	Centralized Version Control Systems - (collaborate w/ developers on other systems) have a single server that contains all the versioned files, and a number of client that check out files from that central place
	
	Distributed Version Control Systems - files in the repository are distributed to other members' server
	

Git's concept "a stream of snapshots". It also only need local files and resources to operate which means no information from another computer is needed. Git is also careful with your files and is wary when it comes to changing or updating files. Also, nearly all of the actions done in Git are added to the Git database.

3 main states of Git
	Committed
	Modified
	Staged 

3 main sections of a Git project
	Git directory - stores the metadata and object database 
	Working directory - single checkout of one version of the project
	Staging area - a file that stores information about what will go into your next commit
