# Git Commands
This is a practice repository for practicing Git commands. <br>
The following are some Git commands.

## Basic Git Commands
* A folder named git-test is created in the local machine.
* The git-test folder is opened in an editor (VS Code), and an index.html file is added.

#### Initializing folder as a Git repository
* In the cmd window, I cd into the git-test folder, and type the following command to initialize the folder as a local Git repository.
~~~~
git init
~~~~

#### Checking Git repository Status
* The following command is typed to check the Git repo's status
~~~~
git status
~~~~

#### Adding Files to the Staging Area
* To add files to the staging area of the Git repo:
~~~~
git add .
~~~~
* The . signifies all files.

#### Commiting to Git Repository
* To commit the current staging area to the local Git repo, with the message "first commit"
~~~~
git commit -m "first commit"
~~~~

#### Checking log of Git commits
* To check the log of the commits to your Git repository
~~~~
git log --oneline
~~~~


#### Checkout a file from the previous/older commit
* If we don't like the current file that we have in our folder/ want to go back to the previous version of the file, we can always check out the file from a previous commit.
~~~~
git checkout <commit identifier/number> <file name>
~~~~

#### Inspect what has been changed
* To check exactly what has been changed to a file. It shows the differences between the original file and the file that now has changes made to it.
~~~
git diff <a specific file or folder>
~~~

## Online Git Repositories
First, an online git repository named git-test is setup on Github (This repository that we are looking at now). <br>
Then we copy the URL of the online repo

#### Linking Local repository to Online Git repository
* This sets the local git repo's remote origin to the online GitHub repo.
~~~~
git remote add origin <URL of online repo>
~~~~

#### Pushing commits to online repo
* This command pushes contents of local git repository, to the origin to the master branch (of the online repo)
* Login credentials may be requested at this point. But if given previously, then there is no need to do it again.
~~~~
git push -u origin master
~~~~
Contents of the local git repo will now be pushed to the server side.

#### Cloning an Online Repository
* This command clones (means copy) an online repo onto the local computer.
* The online repo will be cloned into a local folder, with the same name, git-clone (remember to cd into the local folder where you want the cloned repo to appear).
~~~~
git clone <repository URL>
~~~~

## Branching
A branch represents an independent line of development. Branches serve as an abstraction for the edit/stage/commit process. 
The purpose of Branching is to enable developers to work in parallel dimensions and develop features separately. Also, working on a feature will require several commits. The master branch is the working code in production. If unfinished work is pushed into the master branch, it might become buggy and unstable. Having a branch will allow developers to work in an isolated environment without affecting the master branch. And once work is complete and the code is ready for production, the branch can be merged back into the master branch.
#### See all branches
* To see a list of all the current branches in the project, type git branch, with no arguments.
* A small star will be placed next to the curernt branch in which you are at.
~~~~
git branch
~~~~
#### Creating a new branch
* This command will create a new branch in the project
* Take note, this only creates the branch. To start adding commits to it, the next step is to switch from your current branch to the new branch (see next point).
~~~~
git branch <branch name>
~~~~
#### Switching between branches
* To go to a branch and start making changes/commits, use this command:
~~~
git checkout <branch name>
~~~
