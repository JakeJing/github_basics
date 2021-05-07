# Github Basics

Yingqi Jing

It is important to distinguish between documents in your own computer (local host) and in the github website (remote host). 

## 1. Communication between local and remote hosts

(1) **clone** a repos from the web to you local disk

```bash
git clone https://github.com/JakeJing/github_basics.git
```

(2) **add**, **commit** and **push** everything you have changed locally to the remote host

```bash
git add . # add everything changed to the commit list
git commit -m "my first commit" # commit changes
git push # publish your local commits to the web (user name and password may be required)
```

(3) synchronize or **pull** the changes occurred in the web to the local repository

```bash
git pull
```

## 2. Communication between local and upstream repositories

If your repository is forked from somewhere else or inherited from an upstream repository, you need to synchronize your local repository with the original one. 

(1) set a repository as **upstream**

```bash
git remote add upstream  https://gitlab.utu.fi/amilum/arhi.git
```

(2) check the branches in local and remote repos

```bash
git branch -av
```

(3) pull the changes from upstream to master

```bash
git pull upstream master
```

## 3. Some useful commands

(1) check the **log** files

```bash
git log
```

(2) check the **status** of the local repos.

```bash
git status
```

(3) remove files from the server and the disk

```bash
# remove both
git rm file1.txt
git commit -m "remove file1.txt"

# remove file remotely
git rm --cached file1.txt
git commit -m "remove file1.txt in the web"
```

(4) check the current authentication (HTTPS vs. SSH)

```bash
git remote -v
# change from SSH to HTTPS
git remote set-url origin https://YOURURL
# change from HTTPS to SSH
git remote set-url origin git@github.com:USERNAME/REPOSITORY.git
```

(5) Caching your github personal access token (PAT) , generate your PAT first in the web (Settings -> developer settings -> personal access token)

```bash
git config --global credential.helper osxkeychain
```

