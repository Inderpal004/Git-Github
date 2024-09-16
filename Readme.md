# Git Configuration and Commands

This document provides a guide on configuring Git, cloning repositories, tracking file status, and other essential Git commands.

---

## Configuring Git

### Global Level
Configure Git with your username and email globally (for all repositories).
```bash
git config --global user.name "My Name"
git config --global user.email "myemail@example.com"
```

### Local Level
Set Git configuration specific to a single repository.
```bash
git config user.name "My Name"
git config user.email "myemail@example.com"
```

### Check Configuration
Display the current Git configuration.
```bash
git config --list
```

---

## Cloning & Status

### Clone
Clone a remote repository to your local machine.
```bash
git clone <repository-link>
```

### Status
Check the current state of your working directory and staging area.
```bash
git status
```
- **untracked** — New files that Git isn't tracking yet.
- **modified** — Files that have been changed but not yet staged.
- **staged** — Files that are ready to be committed.
- **unmodified** — Files that have not been changed.

---

## Add, Commit, and Stash

### Add
Add files to the Git staging area to prepare them for a commit.
```bash
git add <file-name>
```

### Commit
Record changes to the repository with a message describing the changes.
```bash
git commit -m 'Commit message'
```

### Stash
Temporarily save changes without committing them.
```bash
git stash
```
- **View stashes**:
  ```bash
  git stash list
  ```
- **Apply latest stash**:
  ```bash
  git stash apply
  ```
- **Apply a specific stash**:
  ```bash
  git stash apply stash@{<index>}
  ```
- **Delete stash after applying**:
  ```bash
  git stash pop
  ```

---

## Push Command

### Push
Upload local repository content to the remote repository.
```bash
git push origin main
```

---

## Init Command

### Initialize a New Git Repository
Create a new Git repository locally and link it to a remote.
```bash
git init
git remote add origin <repository-link>
git remote -v    # Verify the remote link
git branch       # Check current branch
git branch -M main  # Rename the branch to 'main'
git push origin main
git push -u origin main   # Set upstream branch
```

---

## Branches Commands

### Managing Branches
- **Check branch**: 
  ```bash
  git branch
  ```
- **Rename branch to 'main'**: 
  ```bash
  git branch -M main
  ```
- **Switch to another branch**: 
  ```bash
  git checkout <branch-name>
  ```
- **Create and switch to a new branch**: 
  ```bash
  git checkout -b <new-branch-name>
  ```
- **Delete a branch**: 
  ```bash
  git branch -d <branch-name>
  ```

---

## Merging Code

### Way 1: Using Git Merge
- **Compare changes between branches**:
  ```bash
  git diff <branch-name>
  ```
- **Merge branches**:
  ```bash
  git merge <branch-name>
  ```

### Way 2: Create a Pull Request (on GitHub)

Pull requests allow you to discuss and review changes pushed to a branch in a remote repository before merging them.

---

## Fetch Command

### Fetch Changes Without Merging
Use fetch to get the latest changes from the remote repository, but without automatically merging them into your local branch.
```bash
git fetch origin
```

---

## Pull Command

### Fetch and Update Local Repository
```bash
git pull origin main
```
This command fetches and downloads content from the remote repository and immediately updates the local repository to match.

---

## Resolving Merge Conflicts

Merge conflicts occur when Git is unable to automatically resolve differences between two commits. You will need to manually resolve conflicts in the affected files and commit the changes.

---

## Undoing Changes

### Undo Staged Changes
- **Unstage specific files**:
  ```bash
  git reset <file-name>
  ```
- **Unstage all files**:
  ```bash
  git reset
  ```

### Undo Committed Changes
- **Undo the last commit**:
  ```bash
  git reset HEAD~1
  ```
- **Undo several commits by resetting to a specific commit hash**:
  ```bash
  git reset <commit-hash>
  git reset --hard <commit-hash>  # This will discard all changes
  ```

---

## Deleting Files

### Remove a file from the working directory and staging area
```bash
git rm <file-name>
```

### Remove a file only from Git but keep it locally
```bash
git rm --cached <file-name>
```

---

## Viewing Logs and History

### Log of commits
View the commit history of your project.
```bash
git log
```

### Log with specific details (one line per commit)
```bash
git log --oneline
```

### View the history of changes to a file
```bash
git log <file-name>
```

---

## Tagging

### Create a Tag
Tags are used to mark specific points in Git history.
```bash
git tag <tag-name>
```

### List all Tags
```bash
git tag
```

### Push Tags to Remote
```bash
git push origin <tag-name>
```

---

## Working with Remote Repositories

### Add a New Remote
```bash
git remote add <remote-name> <remote-url>
```

### View Remote Repositories
```bash
git remote -v
```

### Remove a Remote
```bash
git remote remove <remote-name>
```

---

This guide covers essential and advanced Git commands for managing your code efficiently. For more advanced usage, refer to the official Git documentation.
```