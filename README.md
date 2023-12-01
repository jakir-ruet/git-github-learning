[![Youtube][youtube-shield]][youtube-url]
[![Facebook-Page][facebook-shield]][facebook-url]
[![LinkedIn][linkedin-shield]][linkedin-url]

<h3 align="center">
   Visit Us <a href="http://www.lapissoft.com">Lapis Soft</a>
</h3>

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

```
git --version
```

#### check the command and it details

```
git or gir --help
```

#### check the config list

```
git config --list
```

#### setup the username and email

```
git config --global user.name "jakir-ruet"
```

```
git config --global user.email "<jakir.ruet.bd@gmail.com>"
```

#### setup the default branch

```
git config --global init.defaultBranch master
```

### Create First repository

#### initialize the repository

```
git init
```

#### add all resource to repository

```
git add -A of git add .
```

#### making a initial commit

```
git commit -m "initial commit"
```

#### making default branch name

```
git branch -M master
```

#### add to remote

```
git remote add origin https://github.com/UserName/RepositoryName.git
```

```
git remote add origin https://github.com/jakir-ruet/git-github-learning.git
```

#### push the project to live github.com

Here, -u (upstream) flag creates a tracking reference for every branch that you successfully push onto the remote repository

```
git push -u origin master
```

#### check the status

```
git remote
```

origin — that is the default name Git gives to the server you cloned from

#### check the fetch & push details

```
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

```
ssh-keygen -t rsa -b 4096 -C "jakir.ruet.bd@gmail.com"
```

Check is 

```
cat /root/.ssh/id_rsa & cat /root/.ssh/id_rsa
```

Connect with agent

```
ssh-add id_rsa
```

Active the agent

```
eval $(ssh-agent -s)
```

```
clip < id_rsa.pub
```

## Courtesy of Jakir

<a href="https://www.linkedin.com/in/jakir-ruet/">LinkedIn</a>
<a href="https://www.facebook.com/jakir.ruet">Facebook</a>
<a href="https://github.com/jakir-ruet">GitHub</a>
<a href="https://web.skype.com/?openPstnPage=true">Skype</a>

## Have a good day, stay with me

[youtube-shield]: https://img.shields.io/badge/-Youtube-black.svg?style=flat-square&logo=youtube&color=blue&logoColor=red
[youtube-url]: https://www.youtube.com/@LapisSoft/featured
[facebook-shield]: https://img.shields.io/badge/-Facebook-black.svg?style=flat-square&logo=facebook&color=pink&logoColor=blue
[facebook-url]: https://www.facebook.com/GoLapisSoft/
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=red
[linkedin-url]: https://www.linkedin.com/company/lapis-soft/

```

```
