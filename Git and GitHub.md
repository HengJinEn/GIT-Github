# Git and GitHub

Tags: Notes, Programming with Mosh, Youtube Videos, freeCodeCamp
Sources: https://youtu.be/RGOj5yH7evk https://youtu.be/8JJ101D3knE

# Index 🤖

[Introduction 🤩](https://www.notion.so/Introduction-f92c502417234b609b5113228957fb60?pvs=21) 

[Youtube Videos Notes🎬](https://www.notion.so/Youtube-Videos-Notes-603ffa968c904f79817d3eb70d3b7a10?pvs=21) 

[w3school 📎 Notes and exercise](https://www.notion.so/w3school-Notes-and-exercise-6ac67762608a46f8acd419786d753a31?pvs=21) 

# Introduction 🤩

---

## 1. What is Git?

Free and open source version control system

## 2. What is Version Control?

The management of changes to documents, computer programs, large websites, and other collections of information.

---

## **Terms**

- Directory → Folder
- Terminal or Command Line → Interface for Text Commands
- CLI → Command Line Interface
- cd → Change directory
- Code Editor → Word Processor for Writing Code
- Repository → Project, of the folder/place where your project is kept
- GitHub → A website to host your repositories online

## Git commands

- Clone → Bring a repository that is hosted somewhere like Github into a folder on your local machine
- add → Track your files and changes in Git
- commit → Save your files in Git
- push → Upload Git commits to remote repo, like Github
- pull → Download changes from remote repo to your local machine, the opposite of push

---

# Youtube Videos Notes🎬

## ******Git Configuration******

```bash
$ git config --global core.editor "code --wait"
```

> wait until the vs code instance to close
> 

```bash
$ git config --global -e
```

> open configuration file
> 

```bash
$ git config --global core.autocrlf true
```

![Untitled](Git%20and%20GitHub%208014c0f132414c9eb32a162bd74de0b7/Untitled.png)

```bash
$ mkdir Moon

$ cd Moon

$ git init
Initialized empty Git repository in C:/Users/ADMIN/Moon/.git/
```

> mkdir → make a directory
cd → change the current directory
init → Initialized empty Git repository to the current directory
- .git is a hidden directory therefore if you
> 

```bash
$ ls
```

> we don’t see anything
but if you type
> 

```bash
$ ls -a
./  ../  .git/
# see the subdirectory
```

> if you want to remove the git repository
> 

```bash
$ rm -rf .git
```

## Workflow of Git

![Untitled](Git%20and%20GitHub%208014c0f132414c9eb32a162bd74de0b7/Untitled%201.png)

Staging area → propose for the next commit

- add the files to the staging area once everything is ok make a snapshot

![Untitled](Git%20and%20GitHub%208014c0f132414c9eb32a162bd74de0b7/Untitled%202.png)

```bash
**Staging files**
git add file1.js # Stages a single file
git add file1.js file2.js # Stages multiple files
git add *.js # Stages with a pattern
git add . # Stages the current directory and all its content
```

```bash
**Viewing the status** 
git status # Full status 
git status -s # Short status
```

```bash
**Committing the staged files** 
git commit -m “Message” # Commits with a one-line message 
git commit # Opens the default editor to type a long message
```

```bash
**Skipping the staging area** 
git commit -am “Message
```

```bash
**Removing files**
git rm file1.js # Removes from working directory and staging area
git rm --cached file1.js # Removes from staging area only
```

```bash
**Renaming or moving files** 
git mv file1.js file1.txt
```

```bash
$ echo logs/ > .gitignore
# don't want git to track our file
```

```bash
**Viewing the staged/unstaged changes** 
git diff # Shows unstaged changes
git diff --staged # Shows staged changes 
git diff --cached # Same as the above
```

```bash
**Viewing the history**
git log # Full history 
git log --oneline # Summary 
git log --reverse # Lists the commits from the oldest to the newest 
**Viewing a commit** 
git show 921a2ff # Shows the given commit 
git show HEAD # Shows the last commit 
git show HEAD~2 # Two steps before the last commit 
git show HEAD:file.js # Shows the version of file.js stored in the last commit
```

## Git in VSCode

```powershell
git clone < ssh of your github repository>
```

```powershell
ls -la
# list everything in the directory including hidden files and folder
```

```powershell
git push origin main/master (depends on the code)
```

### Git Branching

![Untitled](Git%20and%20GitHub%208014c0f132414c9eb32a162bd74de0b7/Untitled%203.png)

```powershell
**Managing branches**
git branch bugfix # Creates a new branch called bugfix
git checkout bugfix # Switches to the bugfix branch
git switch bugfix # Same as the above
git switch -C bugfix # Creates and switches
git branch -d bugfix # Deletes the bugfix branch
Comparing branches
git log master..bugfix # Lists the commits in the bugfix branch not in master
git diff master..bugfix # Shows the summary of changes
```

---

# w3school 📎 Notes and exercise

1. Check which version of Git (if any) is installed

```bash
git --version
```

2. Initialize Git on the current folder

```bash
git init
```

3. Set the user name for the current repository to "w3schools-test”

```bash
git config user.name "w3schools-test"
```

4. Check the status of the Git

```bash
git status
```

5. Add `index.html` to the Staging Environment

```bash
git add index.html
```

6. Stage all new, modified, and deleted files. Use the shorthand command

```bash
git add -A
```

7. Commit the changes to the current repository with the message "First release!”

```bash
git commit -m "First release!"
```

8. Check the compact version of the status for repository

```bash
git status -s
```

9. Commit the updated files directly, skipping the staging environment

```bash
git commit -a -m "New line added"
```

10. View the history of commits for the repository

```bash
git log
```

11. Show the possible options for the status command in command line

```bash
git status -h
```

12. Show all git possible commands in command line

```bash
git help --all
```

13. Create a new branch called hello-world-images

```bash
git branch hello-world-images
```

14. List the existing branches

```bash
git branch
```

15. Move to the hello-world-images branch

```bash
git checkout hello-world-images
```

16. Create, and move to a new branch with the name hello-you

```bash
git checkout -b hello-you
```

17. Merge the hello-you branch with the current branch

```bash
git merge hello-you
```

18. Remove the hello-you branch from the local repository

```bash
git branch -d hello-you
```

19. Add a `remote` repository as an `origin`

```bash
git remote add origin https://github.com/x/y.git
```

20. `pull` is a combination of

```bash
fetch and then merge
```

21. Get all the change history of the origin for this branch

```bash
git fetch origin
```

22. Merge the current branch with the branch master, on origin

```bash
git merge origin/master
```

23. Update the current branch from its origin using a single command

```bash
git pull origin
```

24. `push` the current `branch` to its default remote `origin`

```bash
git push origin
```

25. List all local and remote branches of the current Git

```bash
git branch -a
```

26. List only remote branches of the current Git

```bash
git branch -r
```

27. Clone the repository: `https://abc.com/x/y.git` to your local Git

```bash
git clone https://abc.com/x/y.git
```

28. Clone the repository `https://abc.com/x/y.git` to a folder named "`newlife`"

```bash
git clone https://abc.com/x/y.git newlife
```

29. Rename the `origin` `remote` to `upstream`

```bash
git remote rename origin upstream
```

30. In `.gitignore` add a line to ignore all `.temp` files

```bash
*temp
```

31. In `.gitignore` add a line to ignore all files in any directory named `temp`

```bash
temp/
```

32. In `.gitignore` add a single line to ignore all files named `temp1.log`, `temp2.log`, and `temp3.log`

```bash
temp?.log
```

33. In `.gitignore`, ignore all `.log` files, except `main.log`

```bash
*.log
!main.log
```

34. Add a new `remote` named `ssh-origin` connecting to `x/y.git` on `abc.com` using `SSH`

```bash
git remote add ssh-origin git@abc.com:x/y.git
```

35. Replace the `remote` `URL` for `origin` with `x/y.git` on `abc.com` using `SSH`

```bash
git remote set-url origin git@abc.com:x/y.git
```

36. Show the `log` of the repository, showing just 1 line per `commit`

```bash
git log --oneline
```

37. `revert` the latest `commit`

```bash
git revert HEAD
```

38. `revert` the latest `commit`, skipping the commit message editor

```bash
git revert HEAD --no-edit
```

39. `revert` the two last commits

```bash
git revert HEAD~1
```

40. `reset` to the `commit` with the hash `abc1234`

```bash
git reset abc1234
```

41. Amend the previous `commit` to with the message `"Updated index"`

```bash
git commit --amend -m "Updated index"
```