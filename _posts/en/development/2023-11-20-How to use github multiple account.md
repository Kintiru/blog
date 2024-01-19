---
title: 'How to use github multiple account'
date: 2023-11-20 16:00:00 +0900
author: kintiru
categories: [English, Development]   # [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [English]     # TAG names should always be lowercase
math: true
mermaid: true
#img_path: 
#image: #preview image
    #path:
    #alt:
    #lqpq:
#pin: true
---

# Creating SSH Key

In Windows terminal or git bash, create ssh key using the following command

```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

If you want to specify a path and a filename, you can use 

```
ssh-keygen -t ed25519 -C "your_email@example.com" -f "path"
```

You can simply create in current directory like below

```
ssh-keygen -t ed25519 -C "your_email@example.com" -f "your_username"
```

# Registering SSH Key to git

Add ssh key using the command below.

```
ssh-add /path/to/your_key
```

Verify that it is successfully added.

```
ssh-add -l
```

If you are using git bash you should do the above in window terminal and have to connect bash's ssh with the windows ssh.

```
git config --global core.sshCommand C:/Windows/System32/OpenSSH/ssh.exe
```

# Setting config of repo

You will have to specify which account you are going to use for the repo each time you clone or create new repo.

You can set a global config, but you should still do this if you want to use different account.

```
git config user.name your_username
git config user.email your_email@example.com
```