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

# Branche Commands

git branch  (to check branch)
git branch -M main   (to rename branch)
git checkout <--branch name-->  (to navigate)
git checkout -b <--new branch name-->  (to create new branch)
git branch -d <--branch name-->  (to delete branch)

