# Git account set-up
Get Git installed on your computer and sign up for a GitHub account if you do not already have one.  
* Install Git by submitting a request to National Service Desk  
* Configure Git using instructions provided here (Should I add the link to set-up git here)  
* Enable two factor authentication if required  
> In case you have enabled a two-factor authentication code for security, you may be required to create a personal access token. This token is used instead of your GitHub password (and the authentication code) wherever required through Git Bash.  

# How to start a project?
## Creating a repository 
* Click on "New" to create a new repository 
* Fill in the form that appears - entering name of the repository and description.
* Select “Public” to create a repository open to all for reading. Note that only those added as members can commit or make changes to the repository.
* Select “Initialize the repository with a README file” to get started with the basic documentation. README.md file is created automatically. This file is displayed when someone opens up the repository and can be used to give any instructions to those who are editing the repository.
> In case joining an ongoing project, ask the repository admin to add your GitHub account to the project and provide editing privileges. Next, jump to cloning the project on your computer.

## Creating a branch 
Each repository has a default master branch. In case you need to create new branches, create a branch using the branch menu selector on the GitHub repository page. 
[Learn more](https://help.github.com/en/articles/creating-and-deleting-branches-within-your-repository)

## Creating a fork
A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. To create a fork, click 'Fork' on the main page of the GitHub repository.  
[Learn more](https://help.github.com/en/articles/fork-a-repo)

Once the fork is created, configure a remote pointing an upstream repository to sync any changes between the fork and the original repository. [Learn more](https://help.github.com/en/articles/configuring-a-remote-for-a-fork)

Sync the fork of a repository to keep it up-to-date with the upstream repository, as needed. [Learn more](https://help.github.com/en/articles/syncing-a-fork)

## How to clone a project?
Click "Clone or download" and copy the URL of the remote repository
Go to the location on your computer where you would like to create the local repository and open Git Bash here.
Create a directory where you want to save the local version of the repository
	mkdir DirectoryName
Clone the repository using git clone command into the folder (directory name) on your local machine
	git clone <URL of remote repository> 
	Before cloning, make sure that you are in the correct directory.
[Learn more](https://help.github.com/en/articles/cloning-a-repository)
  
## What is the common workflow?
Go to the local repository folder and right click to open Git bash here. This will ensure that you are in the right directory. Alternatively, you can come to the right directory by using the change directory command (cd) in the Git Bash. 
### Pull
Bringing all the changes from the remote repository to the local repository
		git pull origin BranchName
### PUSH 
Saving all the changes made on the local repository to the remote repository
		git add . && git commit -m "I have made local changes" && git push origin master
	Alternatively, the commands can be typed in separately
		git add .
		git commit -m "Comments go here"
		git push origin master
	Adding a comment with the git commit command helps in back tracking the revisions. 
	You will be required to type in your username and password. 
		Password field will appear empty as you type. Just type the complete password and press enter.
		Please note that in cases where two factor authentication is enabled, you have to type in your personal access token instead of GitHub password to get access. 
	This will also merge your changes to the document with the remote repository. In case, there is a conflict due to competing line changes, an error message will appear indicating the file where the conflict appears. 
		Jump to "How to resolve conflict?" to learn about resolution process
### How to run tests? Add link to Guillaume's Git document
Install node (same place installed Git)
		Instructions for npm config  
			npm config set proxy http://%USERNAME%@proxy.prv:80 
			npm config set https-proxy http://%USERNAME%@proxy.prv:80 
			setx HTTP_PROXY http://%USERNAME%@proxy.prv:80 
			setx HTTPS_PROXY http://%USERNAME%@proxy.prv:80  
		Note that the username required here is the one for your ESDC network. For example, npm config set proxy http://jayson.mcintosh@proxy.prv:80  
Run npm commands from node
		Ensure you are in the same folder as package.json
> Ask REMY about his comment: need to add procedure to fetch remote branch into local store (i.e. after you've created a branch on the remote Repo, doing a git pull origin <branchname> will not download it. You need to create a local branch that tracks a remote branch.

## How to resolve conflict?
Open the local files where the conflict appears.
The picture below shows the appearance of conflict in the file. The competing changes are separate by conflict markers <<<<<<<, =======, >>>>>>>.
> Add a picture or a link to the GitHub page.
Make changes that you want to finally merge to the remote repository, delete the conflict markers and save the file.
There may be more than one merge conflict in a file. Manually resolve all the conflicts and save the file. 
Push the changes on the remote repository again
	git add . && git commit -m 'I have made local changes' && git push origin master

## How to create an issue?
Github Help Guide: https://help.github.com/en/articles/creating-an-issue

## Formatting in markdown files
Standard formatting rules in a markdown file can be viewed here: https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md. 

## Best practices
1. Start your day by a pull request to bring the changes made by your team to your local repository.
2. Commit early and often, to reduce merge conflicts and foster continuous integration.

## List of commonly used commands
cd
ll
ls
mkdir
Git clone
History
Git pull origin master
Git status
Git add .
Git commit -m "Comment goes here"
Git push origin master
Reset
Revert
Checkout
Fetch
Merge

## References
[Github help guide](https://help.github.com/en) 
