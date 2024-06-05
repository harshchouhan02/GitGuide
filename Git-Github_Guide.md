# Git and Github Giude for Begginers

### Download 
    - VS Code (Code Editor)
    - Git Bash

### Github
    - Website to store codes
    - Create profile
    - Create Demo Repository
    - Read me File (.md file)

### Git 
    - Version Control Tool
    - git --version
    - ls, ls -a
    - pwd
    - cd

## Configure Git
    - (Global / Local)
    - git config --global user.name "My Name"
    - git config --global user.email "example@email.com"
    - git config --list

    - Use Git using VS Code (not to write command everytime)


## Basic Commands

### Linux / Terminal
    - ls, ls -Force (Show Files)
    - pwd (Current Directory / Path)
    - cd, cd .. (Change Directory)
    - mkdir (Create Folder)
    - notepad index.html (Create/Edit File) -> on Notepad
    - code index.html (Create/Edit File)    -> on VS Code


### Clone & Status
    - git clone <repo_link>   -> https clonings
    - git status 
        (If File is modified, do following steps)
        - untracked, modified, stages, unmodified   -> Status

        - Add (add new or changed files in your working directory)
            - git add *
            - git add .
            - git add <filename>

        - Commit (it is the record of change)
            - git commit -m "message"

### Push
    - git push origin <branch name>

    - git push origin main
    - git push -u origin main (then we can use git push only from the next time, when we are working on single repo for the long time)

    - if you face any problem related to username access denied
        - Check Repository Permissions
        - Correct Git Configuration
        - Clear Cached Credentials (Control Panel > User Accounts > Credential Manager > Delete Github Cache)
        - Re-authenticate
        - Using SSH Instead of HTTPS
            - git remote set-url origin git@github.com:harshchouhan02/DemoFile.git

## Working with Local Repository (Upload Repo from PC to Github)
    ->NOTE:  Always Clone First before Pushing 
    -> When we are working on the project locally (local PC) not remotely

    - git init
        - used to initialize git
    
    - Create Local Files and Do your Project Complete
    - git add .
    - git commit -m "Added Intial files"

    - Create new Repo on Github
    
    - git remote add origin <repo link>
    - git remote -v (to verify remote)
    - git branch
    - git branch -M main (to rename branch)

    - git push origin main


## Standard Workflow
    - Github Repo
    - Clone it
    - Changes Locally
    - Add
    - Commit
    - Push

## Git Branches
    - When two or more developers are working on same project
    - New Branch 
    - Merge two Branches

    - git branch (to check the current branch)  -> like pwd
    - git branch -M <branch newName> (to rename branch)
    - git checkout <branch name>  (to navigate)     -> like cd 
    - git checkout -b <branch name>  (create new Branch)
    - git branch -d <branch name>    (to delete branch)


## Merging Code / Merge Branch

### Way 1 -> using command line
    - git diff <branch name>
        - to compare commits, branches, files and more
    - git merge <branch name>
        - to merge 2 branches

### Way 2 -> using command line
    - create a PR (Pull Request)


## Pull Command
    - git pull origin main
        - used to fetch and download content from a remote repo and immediately update the local repo to match that content

### Resolving Merge Conflict
    - When different changes occures on the same line of the file in two different branch

    - git diff <branch name>    (to whom you want to compare)



## Undoing Changes
    - git log
        - to check all the changes / Commit History

### Staged Changes 
    - (which are added)

    - git reset <filename>
    - git reset             -> Reset all the files in current Repo

### Commited Changes
    - (for one commit)
    - git reset HEAD~1

### Commited Changes
    - (for many commits)
    - git reset <commit hash>       --> hash is a unique code of that commit
    - git reset --hard <commit hash>       -> prefered


## Fork
    - from Github
    - Rough copy of any repository
    - Copying another repository

    - Fork the repository
    - Change it on your repo
    - Create Pull Request to merge your repo with another person's Original repo from where you have forked the repo
