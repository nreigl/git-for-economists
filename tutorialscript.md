---
title: Script live tutorial
author: "Heili Hein & Nicolas Reigl"
date: 01.01.2020
---


# Notes

Target Thursday 20:30 for the tutorial


1. Intro

Here we will show how to init a repo, show git status, git log, add files in the staging area and commit files.



make directory & cd into directory
```bash
mkdir git_tutorial
cd git_tutorial
```

Show that working tree is not VC
```bash
git status
```


Initiate a repo
```bash
git init
```

Show status
```bash
git status
```


```bash
git --version
git --help
```


Cd into hidden folder and exit back
```bash
cd .git/
..
```

Create a new markdown document
```bash
touch vegetables.md
```

Show status
```bash
git status
```

Add vegetables.md from the stating area
```bash
git add vegetables.md
```

Show status
```bash
git status
```


Make a change in vegetables.md
```bash
nvim vegetables.md
```

Show status
```bash
git status
```

Add vegetables.md from the stating area
```bash
git add -u # Stage updated files
git add . # Stage new files
git add vegetables.md
```



Commit
```bash
git commit -m"add vegetables.md"
```

Show status
```bash
git status
```

Show log
```bash
git log
```


Add another file
```bash
touch vegitables.md
```

Show status
```bash
git status
```


Add all files
```bash
git add -A # carefull with the .gitignore
```

Commit all files
```bash
git commit -m "add vegetables.md"
```

Change in vegetables.md & and add vegetable
```bash
nvim animal.md
```

Git add all files
```bash
git add -.
```

Commit
```bash
git commit -m"make a mistake"
```

## 2. Revert back

Show the log and copy git hashkey
```bash
git log
```

Checkout to previous version
```bash
git checkout
```


Show status and show log
```bash
git status
git log
```


## 3. Create a branch

Here we will show how to create a branch, switch a branch, diff branches and merge branches

Look at available branches
```bash
git branch
```

Create a new branch called development
```bash
git developtment
```

Switch to development branch
```bash
git checkout developtment
```

Add a file fruits.md & add a fruit
```bash
touch fruits.md
nvim fruits.md
```

Add and commit
```bash
git add -A
git commit -m"add fruits.md"
```

Switch back to master
```bash
git checkout master
```

Check difference between master and development
```bash
git diff master developtment
```


Merge master with development
```bash
git merge master # master is the receiving branch  
```

### Create a merge conflict 



```bash
git checkout development # master is the receiving branch  
```

```bash
nvim vegetables # master is the receiving branch  
```




## Switch to GUI

Open the folder in VS Code and show the audience around.



## 4. Github


Show status
```bash
git status
```

 - go to GitHub
 - new public repo
 - repo name
 - add no other files
 - copy the terminal commands from [GitHub](GitHub)

The first command creates the remote
The second command makes sure that you're on local main
The third command pushes local main to remote main

Show status
```bash
git status
```


Currently only the master branch is on GitHub but what if I want to add a new development branch to

Create new local branch
```bash
git checkout -b sweats
```

Push branch sweats up to GitHub
```bash
git push -u origin sweats
```

Go to GitHub and show the sweats branch



Got back to GitHub and create a README.md file


Pull from the remote
```bash
git pull origin main
```

Show status
```bash
git status
```

## 5. Collaborating

In this part Heili forks and works and Nicolas test-repo and then creates a pull request. Nicolas will review the pull request, deal with merge conflicts

 - Fork the repo
 - Show the sweats on GitHub your repo
 - Add a file called "places"
 - Write some places you like
 - Change in my file the first vegetables entry from dogs to cats (so that we can teach how to resolve merge conflicts)
 - Commit everything and create a pull request


### Switch back to my session


 - Review pull request
 - Accept pull request
 - Fix merge conflicts
 - Merge


 I will create another artificial problem. I will change in the local file an line that would conflict with the newly merged remote.

 - make changes to local master
 - git pull to local master

