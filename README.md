[![LinkedIn][linkedin-shield-lapissoft]][linkedin-url-lapissoft]
[![Facebook-Page][facebook-shield-lapissoft]][facebook-url-lapissoft]
[![Youtube][youtube-shield-lapissoft]][youtube-url-lapissoft]

## Visit Us [Lapis Soft](http://www.lapissoft.com)

### Overview

Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.

Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows.

#### Course Outline

1. Introduction
2. Version Control System (VCS)
3. Git (Download & Install), Configuration
4. Remote VCS (GitHub, GitLab, SVN (SunVersion))
5. GitHub
   - Account Setup
   - Connecting to Git
   - Collaboration
   - GitHub Functionalities
   - watch, history, issues, branches, conflicts resolution, merge, merge conflicts

#### Environment Setup

##### git version check

```bash
git --version
```

#### check the command and it details

```bash
git or gir --help
```

#### check the config list

```bash
git config --list
```

#### setup the username and email

```bash
git config --global user.name "jakir-ruet"
```

```bash
git config --global user.email "<jakir.ruet.bd@gmail.com>"
```

#### setup the default branch

```bash
git config --global init.defaultBranch master
```
```bash
git config --global --list
```
```bash
git config --global --edit
```

### Create First repository

#### initialize the repository

```bash
git init
```

#### add all resource to repository

```bash
git add -A of git add .
```

#### making a initial commit

```bash
git commit -m "initial commit"
```

#### making default branch name

```bash
git branch -M master
```

#### add to remote

```bash
git remote add origin https://github.com/UserName/RepositoryName.git
```

```bash
git remote add origin https://github.com/jakir-ruet/git-github-learning.git
```

#### push the project to live github.com

Here, -u (upstream) flag creates a tracking reference for every branch that you successfully push onto the remote repository

```bash
git push -u origin master
```

#### check the status

```bash
git remote
```

origin — that is the default name Git gives to the server you cloned from

#### check the fetch & push details

```bash
git remote -v
```

### SSH & GPG Connection (Secure Shell)

It is a cryptographic network protocol for operating network services securely over an unsecured network. Its most notable applications are remote login and command-line execution.
SSH applications are based on a client–server architecture, connecting an SSH client instance with an SSH server. SSH operates as a layered protocol suite comprising three principal hierarchical components: the transport layer provides server authentication, confidentiality, and integrity; the user authentication protocol validates the user to the server; and the connection protocol multiplexes the encrypted tunnel into multiple logical communication channels. The secure shell works two ways

1. **Symmetric Key Encryption**
It is simple & less secure. The encryption & decryption complete by using same **same key** with both users. Its length is ***128*** or ***256*** bits. For example ***AES*** (Advanced Encryption Standard), ***DES*** (Data Encryption Standard), ***3DES***, and ***RC4***.
2. **Asymmetric Key Encryption**
It is complex & secure. The encryption & decryption complete by using same **different key** (private key & public key) with both users. The private is for host user and the public key is gust user. Its length is ***2048*** or ***higher***. For example ***RSA*** (Rivest, Shamir, Adleman), ***DSA*** (Digital Signature Algorithm), ***ECC***, ***El Gamal***.

#### Asymmetric Key Encryption

Generate the private & public key

```bash
ssh-keygen -t rsa -b 4096 -C "yourEmail@gmail.com"
```

Check is 

```bash
cat /root/.ssh/id_rsa & cat /root/.ssh/id_rsa
```

Connect with agent

```bash
ssh-add id_rsa
```

Active the agent

```bash
eval $(ssh-agent -s)
```

```bash
clip < id_rsa.pub
```

Staging-Unstaging
```bash
git add . # staging everything
git add filename # staging specific file
git add *.html # staging .html extension a file only in a directory
git add **/*.html # staging .html extension all file from all directory
git status
git rm --cached index.html # unstaging the index.html file
git add . # staging everything
git mv info.txt info1.txt # renaming file
```

***Head***
In Git, HEAD refers to the currently checked-out branch's latest commit.
You can think of the HEAD as the "current branch". When you switch branches with git checkout, the HEAD revision changes to point to the tip of the new branch.
```bash
cat .git/HEAD # You can see what HEAD points to by doing
git log
git log --oneline
git show commitId/HEAD
git checkout specificCommit # go to specific commit
git checkout master # for present commit
```

***Stash-Merge-Rebase***

***[Stash:](https://git-scm.com/docs/git-stash)***

In git there are two ways to save changes the git repository such as
- commit
  Developer is working on a project and wants to preserve the changes with committing them.
- stash (secret or hidden)
  Developer is working on a project and wants to preserve the changes without committing them.

  Stash vs Stage
  |  SL   | Stash                                 | Stage                                     |
  | :---: | :------------------------------------ | :---------------------------------------- |
  |   1   | Object adding as backup               | Object adding process (`git add .`)       |
  |   2   | Not use commit                        | Use commit                                |
  |   3   | Use for switch a task to another task | Not use for switch a task to another task |


```bash
git stash list
git stash # apply stash
git stash apply # withdraw stash
git stash list
git stash apply 1 # withdraw stash no 1
git stash pop # remove state of stash
git stash show # show summary of stash
git stash clear # clear all stash
```

***[Merge:](https://git-scm.com/docs/git-merge)***
Merging is Git's way of putting a forked history back together again. The `git merge` command lets you take the independent lines of development created by `git branch` and integrate them into a single branch.
```bash
git branch
gir branch feature # creating feature branch
git checkout feature # switched to feature branch
git checkout master # switched to master branch
git branch -d feature # delete feature branch
git merge master # merge feature to master branch. also we can merge in github on website.
```

***[Rebase:](https://git-scm.com/docs/git-rebase)***
Rebasing is the process of moving or combining a sequence of commits to a new base commit. Rebasing is most useful and easily visualized in the context of a feature branching workflow.
  Merge vs Rebase
  |  SL   | Merge                               | Rebase                                |
  | :---: | :---------------------------------- | :------------------------------------ |
  |   1   | Non-destructive command             | Destructive command                   |
  |   2   | branch merge each other             | other branch add to master branch     |
  |   3   | its comparatively easy              | its comparatively hard                |
  |   4   | suitable for less active branch     | suitable for frequently active branch |
  |   5   | its non-linear style branching      | its linear style branching            |
  |   6   | exit master branch & other branches | always exit master branch             |
```bash
git branch rebase-test
git checkout rebase-test
git rebase master
```

## Courtesy of Jakir

[![LinkedIn][linkedin-shield-jakir]][linkedin-url-jakir]
[![Facebook-Page][facebook-shield-jakir]][facebook-url-jakir]
[![Youtube][youtube-shield-jakir]][youtube-url-jakir]

### Have a good day, stay with me
<!-- Personal profile -->

[linkedin-shield-jakir]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-jakir]: https://www.linkedin.com/in/jakir-ruet/
[facebook-shield-jakir]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-jakir]: https://www.facebook.com/jakir-ruet/
[youtube-shield-jakir]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-jakir]: https://www.youtube.com/@mjakaria-ruet/featured

<!-- Company profile -->

[linkedin-shield-lapissoft]: https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white
[linkedin-url-lapissoft]: https://www.linkedin.com/company/lapis-soft/
[facebook-shield-lapissoft]: https://img.shields.io/badge/Facebook-%231877F2.svg?style=for-the-badge&logo=Facebook&logoColor=white
[facebook-url-lapissoft]: https://www.facebook.com/GoLapisSoft/
[youtube-shield-lapissoft]: https://img.shields.io/badge/YouTube-%23FF0000.svg?style=for-the-badge&logo=YouTube&logoColor=white
[youtube-url-lapissoft]: https://www.youtube.com/@LapisSoft/featured
