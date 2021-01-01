---
title: Script live tutorial
author: "Heili Hein & Nicolas Reigl"
date: 01.01.2020 
---


# Notes 

Target Thursday 20:30 for the tutorial


## 1. Intro

Here we will show how to init a repo, show git status, git log, add files in the staging area and commit files. 

make directory & cd into directory 
```
mkdir git_tutorial
cd git_tutorial
```

Show that working tree is not VC 
```
git status
```

Initiate a repo 
```
git init
```

Show status 
```
git status
```

Cd into hidden folder and exit back
```
cd .git/
..
```

Create a new markdown document
```
touch animals.md
```

Show status 
```
git status
```

Add animals.md from the stating area
```
git add animals.md
```

Show status 
```
git status
```


Make a change in animals.md
```
nvim animals.md
```

Show status 
```
git status
```

Add animals.md from the stating area
```
git add animals.md
```

Commit 
```
git commit -m"add animals.md"
```

Show status 
```
git status
```

Show log 
```
git log
```


Add another file
```
touch vegitables.md
```

Show status 
```
git status
```


Add all files 
```
git add -A
```

Commit all files 
```
git commit -m "add vegetables.md"
```

Change in animals.md & and add vegetable
```
nvim animal.md
```

Git add all files
```
git add -A
```

Commit 
```
git commit -m"make a mistake"
```

## 2. Revert back 

Show the log and copy git hashkey 
```
git log
```

Checkout to previous version
```
git checkout 
```


Show status and show log 
```
git status
git log
```


## 3. Create a branch

Here we will show how to create a branch, switch a branch, diff branches and merge branches

Look at available branches
```
git branch
```

Create a new branch called development
```
git developtment
```

Switch to development branch
```
git checkout developtment
```

Add a file fruits.md & add a fruit
```
touch fruits.md
nvim fruits.md
```

Add and commit 
```
git add -A
git commit -m"add fruits.md"
```

Switch back to master
```
git checkout master
```

Check difference between master and development
```
git diff master developtment
```


Merge master with development 
```
git merge master development
```


## 4. Github

Here we will show how to create a public repo on github, setup the repo, link the remote, pull and push to the repo.Here we will show how to create a public repo on github, setup the repo, link the remote, pull and push to the repo.  


Show status 
```
git status
```

 - go to github 
 - new public repo
 - repo name 
 - add no other files 
 - copy the terminal commands from github

The first command creates the remote
The second command makes sure that you're on local main 
The third command pushes local main to remote main

Show status 
```
git status
```


Currently only the master branch is on github but what if I want to add a new development branch to 

Create new local branch
```
git checkout -b people
```

Push branch people up to github
```
git push -u origin people
```

Go to github and show the people branch



Got back to github and create a README.md file 


Pull from the remote 
```
git pull origin main
```

Show status 
```
git status
```

## 5. Collaborting

In this part Heili forks and works and Nicolas test-repo and then creates a pull request. Nicolas will review the pull request, deal with merge conflicts

 - Fork the repo
 - Show the people on github your repo
 - Add a file called "places"
 - Write some places you like
 - Change in my file the first animals entry from dogs to cats (so that we can teach how to resolve merge conflicts)
 - Commit everything and create a pull request 
 
 
### Switch back to my session
 
 
 - Review pull request 
 - Accept pull request 
 - Fix merge conflicts
 - Merge
 
 
 I will create another artificial problem. I will change in the local file an line that would conflict with the newely merged remote. 
 
 - make changes to local master 
 - git pull to local master 
 