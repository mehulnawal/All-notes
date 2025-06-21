# Git Commands Notes

## 📑 Index

- [Git Commands Notes](#git-commands-notes)
  - [📑 Index](#-index)
  - [1. Git Config](#1-git-config)
  - [2. Uploading Folder/Project from Local to Remote](#2-uploading-folderproject-from-local-to-remote)
  - [3. Making a Clone of Repo](#3-making-a-clone-of-repo)
  - [4. Updating a Repo on Remote](#4-updating-a-repo-on-remote)
  - [5. Branches](#5-branches)
  - [6. Merge Two or More Branches](#6-merge-two-or-more-branches)
  - [7. Create a Folder](#7-create-a-folder)
  - [8. Move a File into a Folder](#8-move-a-file-into-a-folder)
  - [9. Remove File from GitHub](#9-remove-file-from-github)
  - [10. Rename a File](#10-rename-a-file)
  - [11. Pull Request](#11-pull-request)
  - [12. Undo Changes](#12-undo-changes)
    - [Case 1: Staged changes (files are staged but not committed)](#case-1-staged-changes-files-are-staged-but-not-committed)
    - [Case 2: Committed changes (one commit)](#case-2-committed-changes-one-commit)
    - [Case 3: Committed changes (multiple commits)](#case-3-committed-changes-multiple-commits)
  - [13. Fork](#13-fork)
  - [14. Git Log](#14-git-log)
  - [15. Types of Status](#15-types-of-status)
  - [16. Change the Remote URL in Git](#16-change-the-remote-url-in-git)
  - [17. Terms](#17-terms)
  - [18. Basic Terminal Commands](#18-basic-terminal-commands)

---

## 1. Git Config

```
git config --global user.name "Name"
git config --global user.email "Email"
git config --list
```

---

## 2. Uploading Folder/Project from Local to Remote

```
git init
git add .
git commit -m "Message"
git remote add origin repoLink
git remote -v         (to verify/check remote)
git branch
git branch -M newName
git push origin main / git push origin -u main
```

> `-u` - set upstream

---

## 3. Making a Clone of Repo

```
git clone repoLink
```

---

## 4. Updating a Repo on Remote

```
git status
git add .
git commit -m "Message"
git push origin main
```

---

## 5. Branches

```
git branch                      (to check branch)
git branch -M main              (to rename a branch)
git checkout branchName         (to navigate to another branch)
git checkout -b newBranchName   (to create a new branch)
git branch -d branchName        (to delete a branch)
```

---

## 6. Merge Two or More Branches

```
git branch
git diff main                  (shows the difference between branches)
git merge branchName
```

---

## 7. Create a Folder

```
mkdir folder_name
git add .
git commit -m "Created a new folder"
git push origin branch_name
```

---

## 8. Move a File into a Folder

```
mv file_name folder_name
mv file_name file_name file_name folder_name         (move multiple files)
mv *.txt folder_name                                  (move all files with same extension)
git add .
git commit -m "Moved files into folder_name"
git push origin branch_name
```

---

## 9. Remove File from GitHub

```
rm file_name
rm file_name file_name file_name folder_name         (remove multiple files)
rm *.txt folder_name                                  (remove all .txt files)
```

---

## 10. Rename a File

```
mv old_file_name new_file_name
```

---

## 11. Pull Request

```
git pull origin main    (to bring changes from remote to local)
```

---

## 12. Undo Changes

### Case 1: Staged changes (files are staged but not committed)

```
git reset fileName     (to undo one file)
git reset              (to undo all files)
```

### Case 2: Committed changes (one commit)

```
git reset HEAD~1
```

### Case 3: Committed changes (multiple commits)

```
git reset hash
git reset --hard hash  (also undoes code changes)
```

---

## 13. Fork

> To create a duplicate copy of another project or repo.

---

## 14. Git Log

```
git log   (to view all the changes in the remote)
```

---

## 15. Types of Status

* **Untracked** - New files Git doesn't yet track
* **Modified** - Changed files
* **Staged** - Files ready to commit
* **Unmodified** - Unchanged

---

## 16. Change the Remote URL in Git

```
git remote set-url origin repoLink   (change remote)
git remote -v                        (verify the remote)
```

---

## 17. Terms

* **global**
* **init**
* **add** - To add files from your working directory to remote
* **commit** - To take record of changes
* **push**
* **origin** - Name of remote GitHub repo where files are pushed
* **init** - Creates a new Git repo

---

## 18. Basic Terminal Commands

```
cd        - change directory/folder
ls        - list all files in the directory
ls -a     - list all files including hidden files
mkdir     - create a new directory
clear     - clear all the messages in the terminal
```
