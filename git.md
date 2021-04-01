#Git Cheatsheet

### Make a New Repository:

`git init`: initalize Git repository

`git remote add origin [link]`: syncs the local repository with online repository

### Save your code:

`git add .`: add files to staging area

`git commit -m "message goes here"`: commit to local repository

`git push origin master`: push code to Git

### Copy a Repository

`git clone {url.git}`: copy an entire repository to your local computer. Then you can `cd` into it,
and run `npm install` to install all the dependencies.

### General Branch Commands

`git branch`: see current branch

`git checkout -b {BRANCH_NAME}`: creates a local branch (-b creates a new branch). The branch can then be pushed 
to Github with `git add . `, `git commit -m "message"`, and  `git push origin {BRANCH_NAME}`

`git checkout {branch_name}`: switch branches 

`git status`: see the status of your file

### Merging

If the master branch has been changed by somebody else, you need to pull before you can push.

Commit to a repository that has many contributors:

- You are in your own branch
- `git pull origin master`: will pull any updates since last time you pulled
- `git merge master`: will merge any changes from the master branch into your local branch, *so you can resolve conflicts if there are any.*
- If there are conflicts, you need to *add* and *commit* again.
- `git push origin my-new-feature`
- Finally, the new branch is created on github.com


### Others

Things I have constantly had to Google so might as well include them here:

- `git reset HEAD --hard`: undo any local changes made to tracked files (reverting back to last commit)
- `rm -rf [folder name]`: recursively delete folder and its contents
- `rm [file name]`: delete file
- `git rm --cached [file name]`: remove file from git repo while leaving it in local system; 
follow by doing a commit and push
- `git remote set-url origin [remote url link]`: changing the git origin branch when cloning a repo
 

### Notes:

The `.gitignore` file lets you add specific files and folders that you don't
want saved on Github 