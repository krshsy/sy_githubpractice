Summary

CHAPTER 4

4 major protocols of Git
LOCAL - most basic; remote repository is in another directory on disk; often used if everyone in the team has access to a shared filesystem 
	git clone /opt/git/project.git
HTTP - intelligently negotiate data transfer, similar to that of SSH
	SMART HTTP - uses various HTTP authentication mechanisms; most popular way to use Git
	DUMB HTTP - treats Git repository like normal files from the web server
		$ cd /var/www/htdocs/
		$ git clone --bare /path/to/git_project gitproject.git
		$ cd gitproject.git
		$ mv hooks/post-update.sample hooks/post-update
		$ chmod a+x hooks/post-update
SECURE SHELL (SSH) - self-hosting; SSH access to servers is alread set up in most places
	git clone ssh://user@server/project.git
GIT - special daemon; listens on a dedicated port (9418); similar to SSH but without the authentication

Getting Git on the server
	git clone --bare my_project my_project.git
	
	Putting the bare repository on a server
		scp -r my_project.git user@git.example.com:/opt/git
		git clone user@git.example.com:/opt/git/my_project.git
		
	SSH Access
		If all developers have SSH access, setting up the first repository there is easier
	
		Generating SSH public key
			$ cd ~/.ssh
			$ ls
			authorized_keys2 id_dsa known_hosts
			config id_dsa.pub
			
	Setting up the server
		$ sudo adduser git
		$ su git
		$ cd
		
		Smart HTTP
			$ sudo apt-get install apache2 apache2-utils
			$ a2enmod cgi alias env
			
	GitWeb - simple web-based visualizer; CGI script
		$ git instaweb --httpd=webrick
		[2009-02-21 10:02:21] INFO WEBrick 1.3.1
		[2009-02-21 10:02:21] INFO ruby 1.8.6 (2008-03-03) [universal-darwin9.0]
	
	GitLab - more modern, fully featured Git server

Running own server gives a lot of control and allows to run the sever within your own firewall. 
If data is placed on a hosted server, maintenance and set up is easy.
