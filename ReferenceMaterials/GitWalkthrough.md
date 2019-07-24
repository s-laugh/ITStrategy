# Beginners guide to using Git and GitHub 

## Git account set-up
Get Git installed on your computer and sign up for a GitHub account if you do not already have one.  
- Install Git by submitting a request to National Service Desk  
- Configure Git using instructions provided here (Link to sharepoint pdf file - **Note that the link on the onboarding page on OneNote is not working.**)  
- Enable two factor authentication if required  
> In case you have enabled a two-factor authentication code for security, you may be required to create a personal access token. This token is used instead of your GitHub password (and the authentication code) wherever required through Git Bash.  

## How to start a project?
### Creating a repository 
Here are the steps to create a new repository through your GitHub account:
1. Click on "New" to create a new repository on your GitHub account 
2. Fill in the form that appears - entering name of the repository and description.
3. Select “Public” to create a repository open to all for reading. Note that only those added as members can commit or make changes to the repository.
4. Select “Initialize the repository with a README file” to get started with the basic documentation. README.md file is created automatically. This file is displayed when someone opens up the repository and can be used to give any instructions to those who are editing the repository.
> Note that this will only create a repository remotely on Github and not on your local computer.
> In case joining an ongoing project, ask the repository admin to add your GitHub account to the project and provide editing privileges. 
> Once the repository is created or you are added to one of the already created repository, clone the repository on your computer to make changes locally.

### Creating a branch 
Each repository has a default master branch. In case you need to create new branches, create a branch using the branch menu selector on the GitHub repository page. 
[Learn more](https://help.github.com/en/articles/creating-and-deleting-branches-within-your-repository)
In this case, the branch is created on the GitHub repository. You will need to [fetch](https://github.com/sara-sabr/ITStrategy/blob/08f711a1b0116848468bd798e9cdf55f76e7f19c/ReferenceMaterials/GitWalkthrough.md#L89) the changes on your local repository to work on the branch locally.

You can also create a branch using Git bash. Here are the steps:
1. Go to the local directory where you have created a copy of the repository and open Git Bash here.
2. To create a new branch in this repository, type the following in Git Bash

```bash
git checkout -b <BranchName>
```

This creates a new branch in the local repository and also switches between the branch that can be edited on your local repository.

3. To push the new branch on the remote repository, use the [pull] (Add link here) command on Git Bash. This will replicate the changes made on the local repository to the remote repository.

### Creating a fork
A fork is a copy of a repository to your user account or an organization's account. Forking a repository allows you to freely experiment with changes without affecting the original project. To create a fork, click 'Fork' on the main page of the GitHub repository.  
[Learn more](https://help.github.com/en/articles/fork-a-repo)

Once the fork is created, configure a remote pointing an upstream repository to sync any changes between the fork and the original repository. [Learn more](https://help.github.com/en/articles/configuring-a-remote-for-a-fork)

Sync the fork of a repository to keep it up-to-date with the upstream repository, as needed. [Learn more](https://help.github.com/en/articles/syncing-a-fork)

Please note that to work locally, you will have to clone the repository to your computer.

## How to clone a project?
1. Click "Clone or download" and copy the URL of the remote repository
2. Go to the location on your computer where you would like to create the local repository and open Git Bash here.
3. Create a directory where you want to save the local version of the repository

```bash
mkdir FolderName
```

Skip the step, if you have already created a folder to save the repository. 

4. Clone the repository using git clone command into the folder (directory name) on your local machine

```bash
git clone <URL of remote repository>
```

Before cloning, make sure that you are in the correct directory.

[Learn more](https://help.github.com/en/articles/cloning-a-repository)
  
## What is the common workflow?
Go to the local repository folder and right click to open Git bash here. This will ensure that you are in the right directory. Alternatively, you can come to the right directory by using the change directory command (cd) in Git Bash. 

### Pull
Bringing all the changes from the remote repository to the local repository (this will pull from the master branch)

```bash
git pull origin master
```

To suggest any changes on the files, create a [new branch] (Add a link to the document section above). This can be done through GitHub as well as using Git Bash. 

Using the following command through Git Bash will create a new branch and switch your local repository to this branch.

```bash
git checkout -b <BranchName>
```

Now your local repository is setup to be in <BranchName>. All the edits will happen in this branch, not on master. 

To simply fetch an already created branch to the local repository, use the following commands,

```bash
git fetch
git checkout <BranchName>
```

To simply switch between branches to work on in your local repository, use the following commands,

```bash
git checkout <BranchName>
```

[Learn more](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging)

### Push 
Saving all the changes made on the local repository to the remote repository

```bash
git add . && git commit -m "I have made local changes" && git push -u origin <BranchName>
```

Alternatively, the commands can be typed in separately

```bash
git add .
git commit -m "Comments go here"
git push -u origin <BranchName>
```

You will be required to type in your username and password. Password field will appear empty as you type. Just type the complete password and press enter. Please note that in cases where two factor authentication is enabled, you have to type in your personal access token instead of GitHub password to get access through Git Bash. 

[Learn more](https://help.github.com/en/enterprise/2.14/user/articles/pushing-commits-to-a-remote-repository)

This will also merge your changes to the document with the remote repository. In case, there is a conflict due to competing line changes, an error message will appear indicating the file where the conflict appears. 

Jump to [How to resolve a conflict?](https://github.com/sara-sabr/ITStrategy/blob/HowToUseGit/ReferenceMaterials/GitWalkthrough.md#how-to-resolve-conflict) to learn about resolution process.

### How to run [tests](https://github.com/sara-sabr/ITStrategy#development)? 
Install [node](https://www.npmjs.com/get-npm) same place where Git is installed. 

Configure NodeJS to run npm tests. Here are the instructions for npm config:

```bash
npm config set proxy http://%USERNAME%@proxy.prv:80 
npm config set https-proxy http://%USERNAME%@proxy.prv:80 
setx HTTP_PROXY http://%USERNAME%@proxy.prv:80 
setx HTTPS_PROXY http://%USERNAME%@proxy.prv:80  
```

Note that the username required here is the one for your ESDC network. For example, if the username for the ESDC network is FirstName.Lastname, set the npm config set proxy at http://FirstName.LastName@proxy.prv:80.

Run npm commands from node. Ensure you are in the same folder as package.json.

```bash
npm run test
```

## How to resolve a conflict?
Open the local files where the conflict appears.

The picture below shows the appearance of conflict in the file. The competing changes are separate by conflict markers <<<<<<<, =======, >>>>>>>.
> Add a picture or a link to the GitHub page.

Make changes that you want to finally merge to the remote repository, delete the conflict markers and save the file.

There may be more than one merge conflict in a file. Manually resolve all the conflicts and save the file. 

Push the changes on the remote repository again.

```bash
git add . && git commit -m 'I have made local changes' && git push origin master
```

A merge conflict can also be resolved on GitHub. [Learn here](https://help.github.com/en/articles/resolving-a-merge-conflict-on-github).

## How to create an issue?
You can create an issue on the GitHub repository to track and prioritize your work. For more instructions, go to the [Github Help Guide](https://help.github.com/en/articles/creating-an-issue).

## How to collaborate with team through pull requests?
A pull request may be created to push the work/changes made on one branch to the master branch.

You can also collaborate with team through line commenting, starting a review or simply leaving a general comment on the pull requests. [Learn more](https://help.github.com/en/articles/commenting-on-a-pull-request) about how to leave a comment and resolve conversations in a pull request.

You can link your comments to specific sections/lines in a conversation through permanent links. [Learn more](https://help.github.com/en/articles/creating-a-permanent-link-to-a-code-snippet) how to create permalinks.

To reveal the permanent link for a md file on GitHub, press "y". The URL of the file will change to show the [permalink](https://help.github.com/en/articles/getting-permanent-links-to-files). This can also be used to link specific lines or a group of lines. For example:
https://github.com/sara-sabr/ITStrategy/blob/08f711a1b0116848468bd798e9cdf55f76e7f19c/ReferenceMaterials/GitWalkthrough.md#L89
https://github.com/sara-sabr/ITStrategy/blob/08f711a1b0116848468bd798e9cdf55f76e7f19c/ReferenceMaterials/GitWalkthrough.md#L89-L90

## Formatting in markdown files
Standard formatting rules in a markdown file can be viewed here: https://github.com/DavidAnson/markdownlint/blob/master/doc/Rules.md. 

## Best practices
1. Start your day by a pull request to bring the changes made by your team to your local repository.
2. Commit early and often, to reduce merge conflicts and foster continuous integration.
3. Run npm tests before merging your work to the master branch.
4. Use a branch over a fork wherever possible, as a team member can edit files and create pull requests in your absence. A fork is a repo instance on your account and can only be accessed by you until you give permission to other members.
5. Learn more from the team on conflict resolution workflow. Each team may create their own set of rules to accept and make changes.

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
