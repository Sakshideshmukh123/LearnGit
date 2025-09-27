# Git commands

## 1]Configuring Git

Sets your name and email for Git commits. This identification is attached to all your contributions.

—>**git config  - -global [user.name](http://user.name) “My Name”**  : Sets your identity for all repositories by defining the author name that will appear in commits.

—>**git config  - -global [user.email](http://user.email) “someone@gmail.com”** : Sets your email address for all repositories, which is included in commit information.

—>**git config  - -list** : Displays all configured Git settings for the current repository or globally.

---

## 2]Clone & Status

**Clone** : Cloning a repository on our local machine

—>git clone < - some link - >

**Status :** Displays the state of code

—>git status

Status—>1)Untracked : new files that git doesn’t yet you track

2)Modified : Changed

3)Unmodified : Unchanged

4)Stage : File is ready to be committed

---

## 3]Add & Commit

**add** : adds new or changed files in your working directory to the Git staging working directory to the Git staging area

—>git add <file name>

—>git add .    #for all files

**commit** : It is record of change

—>git commit -m “some message”

---

## 4]Push command

**push :** upload local repo content to remote repo

—>git push origin main

---

## 5]Init command

init : used to create a new git repo    #to check .git include or not we use command which shows hidden files

—>git init

—>git remote add origin < link>  : Connects your local repository to a remote server and adds a remote named "origin" with the specified URL.

—>git remote -v     #to verify remote

---

## 6]Branch Commands

**branch**: Shows a list of branches or creates a new branch. Branches allow you to develop features in isolation.

—>**git branch**: Lists all local branches. The current branch is marked with an asterisk.

—>**git branch <branch-name>**: Creates a new branch with the specified name, but doesn't switch to it.

—>**git branch -d <branch-name>**: Deletes the specified branch (only if it has been fully merged).

—>**git branch -m <new-name>**: Renames the current branch to the new name.

**checkout**: Switches between branches or restores files.

—>**git checkout <branch-name>**: Switches to the specified branch.

—>**git checkout -b <new-branch>**: Creates a new branch and switches to it in one command.

**merge**: Combines changes from different branches.

—>**git merge <branch-name>**: Merges the specified branch into the current branch.

---

## 7]Merging Commands

way1 : —>git diff <- branch name ->    #to compare, commit, branches, files & move

           —>git merge <-branch name->    #to merge 2 branches

way2 : —>create a PR(Pull Request)

**Pull Request :** It lets you tell others about changes you have pushed to a branch in a repository on Github

—>go to pull request

—>create pull request

—>merge pull request

—>confirm merge

To make changes in local machine from remote we use pull commands

---

## 8]Pull Commands

—>git pull origin main : used to fetch and download content from a remote repo and immediately update the local repo to match that content

---

## 9]Resolving Merge Conflicts

An event that takes place when Git is unable to automatically resolve differences in code between two commits.

---

## 10]Undoing Changes

case1 : Staged changes

—>git reset <-file name->

—>git reset

case2 : Commited changes (for one commit)

—>git reset HEAD~1

case3 : Commited changes (for many commits)

—>git reset <-commit hash->

—>git reset - - hard <-commit hash ->

---

## 11]Fork

A fork is a new repo that shares code and visibility settings with the original “upstream” repository

-fork is a rough copy.

---

### **12] Log Commands**

Helps you review commit history.

- **git log** : Shows the commit history with commit IDs, authors, and messages.
- **git log --oneline** : Shows a simplified one-line-per-commit view.
- **git log --graph --oneline --all** : Shows branch structure in a graph-like format.

---

### **13] Show & Diff**

- **git show <commit-hash>** : Shows detailed info about a commit.
- **git diff** : Shows differences between working directory and staging area.
- **git diff --staged** : Shows differences between staging area and last commit.

---

### **14] Stash Commands**

Temporarily saves your uncommitted changes.

- **git stash** : Saves changes in a hidden place and cleans the working directory.
- **git stash list** : Shows stashed changes.
- **git stash pop** : Applies the most recent stash and removes it from stash list.

---

### **15] Remove & Move Files**

- **git rm <file>** : Removes a file from working directory and staging area.
- **git mv <old-name> <new-name>** : Renames or moves a file.

---

### **16] Remote Commands**

- **git remote -v** : Shows all linked remotes (already included in your notes ).
- **git remote remove <name>** : Removes a remote connection.
- **git fetch origin** : Downloads changes from the remote but doesn’t merge them.

---

### **17] Tagging**

Used for marking releases (e.g., v1.0).

- **git tag <tag-name>** : Creates a tag.
- **git tag** : Lists all tags.
- **git checkout <tag-name>** : Moves to a tag (detached HEAD state).

---

### **18] Revert**

Undo a commit without deleting history.

- **git revert <commit-hash>** : Creates a new commit that undoes changes of the given commit.

---

### **19] Clean**

Removes untracked files.

- **git clean -n** : Shows what files would be removed.
- **git clean -f** : Removes untracked files.