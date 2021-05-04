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

## 2. Communication between local and upstream repository

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

