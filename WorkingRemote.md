# What is a Remote Repository?
A remote repository is the same Git repository like yours but it exists somewhere else.
  * git remote - manage remote repository
  * git push - send changes to remote repo
  * git pull - retrieve updates from the remote repo

Remotes can be accessed in a couple of ways, with a URL or a path to a file system
## Git remote command
The command will let you manage and interact with remote repositories. The output of '$ git remote' is just the word origin. Well that's weird. The word "origin", here, is referred to as a "shortname". A shortname is just a short and easy way to refer to the location of the remote repository
* git remote add is used to add a connection to a new remote repository.
* git remote -v is used to see the details about a connection to a remote.
## Git push 
To send local commits to a remote repository you need to use the git push command. You provide the remote short name and then you supply the name of the branch that contains the commits you want to push:
~~~
$ git push <remote-shortname> <branch>
~~~
# Working on Another Person's Repo
In version control terminology if you "fork" a repository that means you duplicate it. Typically you fork a repository that belongs to someone else. So you make an identical copy of their repository and that duplicate copy now belongs to you. When you clone a repository, you get an identical copy of the repository. But cloning happens on your local machine and you clone a remote repository. 
