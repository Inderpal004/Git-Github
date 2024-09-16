# Configuring Git

- Global Level
git config -- global user.name "My Name"
git config -- global user.email "myemail@example.com"

- Local Level
git config user.name "My Name"
git config user.email "myemail@example.com"

git config --list

# Clone & Status

Clone - Cloning a repository on our local machine
git clone <--some link-->

status - displays the state of the code
git status

- untracked -- new files that git doesn't yet track
- modified -- changed
- staged -- file is ready to be committed
- unmodified -- unchanged

# Add & Commit 

- add -- adds new or changed files in your working directory to the Git staging area.
git add <--file name-->

- commit -- it is the record of change
git commit -m 'some message'

# Push Command

- push -- upload local repo content to remote repo
git push origin main

# Init Command

init - used to create a new git repo
git init
git remote add origin <--link-->
git remote -v    (to verify remote)
git branch    (to check branch)
git branch -M main  (to rename branch)
git push origin main
git push -u origin main   (-u means to set upstream)

# Branches Commands

git branch  (to check branch)
git branch -M main   (to rename branch)
git checkout <--branch name-->  (to navigate)
git checkout -b <--new branch name-->  (to create new branch)
git branch -d <--branch name-->  (to delete branch)

# Merging Code

Way 1
git diff <--branch name-->  (to compare commits,branches,files & more)
git merge <--branch name-->  (to merge 2 branches)

Way 2
Create a Pull Request

# Pull Request

It lets you tell others about changes you've pushed to a branch in a repository on Github.

# Pull Command

git pull origin main

used to fetch and download content from a remote repo and immediately update the local repo to match that content.

# Resolving Merge Conflicts

An event that takes place when Git is unable to automatically resolve differences in code between two commits.
