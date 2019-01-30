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

Before you start doing any work, make sure to look for the project's CONTRIBUTING.md file. Next, it's a good idea to look at the GitHub issues for the project
 * look at the existing issues to see if one is similar to the change you want to contribute
 * if necessary create a new issue
 * communicate the changes you'd like to make to the project maintainer in the

When you start developing, commit all of your work on a topic branch:
 * do not work on the master branch
 * make sure to give the topic branch clear, descriptive name

As a general best practice for writing commits:
 * make frequent, smaller commits
 * use clear and descriptive commit messages
 * update the README file, if necessary
 
**Forking A Repository**
In version control terminology if you "fork" a repository that means you duplicate it. Typically you fork a repository that belongs to someone else. So you make an identical copy of their repository and that duplicate copy now belongs to you. 

# Reviewing Existing Work
**Group by Commit Author**
A quick way to see how many commits each contributor has added to the repository is to use the 
~~~ 
$git shortlog
~~~
 * -s: to show just the number of commits (rather than each commit's message
 * -n: to sort them numerically (rather than alphabetically by author name
**Filter by Author**
Another way that we can display all of the commits by an author is to use the regular git log command but include the --author flag
# Rebase Commands
The command will move commits to have a new base. In the command git rebase -i HEAD~3, we're telling Git to use HEAD~3 as the base where all of the other commits (HEAD~2, HEAD~1, and HEAD) will connect to. Whenever you rebase commits, Git will create a new SHA for each commit! This has drastic implications. To Git, the SHA is the identifier for a commit, so a different identifier means it's a different commit, regardless if the content has changed at all.

 * use p or pick – to keep the commit as is
 * use r or reword – to keep the commit's content but alter the commit message
 * use e or edit – to keep the commit's content but stop before committing so that you can:
 * add new content or files
 * remove content or files
 * alter the content that was going to be committed
 * use s or squash – to combine this commit's changes into the previous commit (the commit above it in the list)
 * use f or fixup – to combine this commit's change into the previous one but drop the commit message
 * use x or exec – to run a shell command
 * use d or drop – to delete the commi
