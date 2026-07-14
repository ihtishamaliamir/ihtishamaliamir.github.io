---
layout: default
title: "Bandit Level 0"
parent: "Bandit"
---

# 🎮 Bandit Level 0

![OverTheWire Bandit Banner](https://overthewire.org/img/bandit.png)

---

## 📋 Level Info

| Info | Details |
|------|---------|
| **Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Username** | `bandit0` |
| **Password** | `bandit0` |
| **Goal** | Connect via SSH and retrieve the password for Level 1 |

---

## 🔧 Tools/Commands Used

| Command | Purpose |
|---------|---------|
| `ssh` | Secure Shell client for remote connections |
| `ls` | List files in the current directory |
| `cat` | Display file contents |

---

## 🔍 Step-by-Step Solution

### Step 1: Connect to the Server

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
![Explain Shell: SSH Command](../../assets/images/overthewire/bandit/bandit0/bandit0_ssh.png)
What's happening:

ssh connects you to the remote server

bandit0 is the username

-p 2220 specifies the port number

You'll be prompted for the password: bandit0

💡 Tip: Nothing appears on screen when you type the password — this is normal for security!

Step 2: Explore the Directory
bash
bandit0@bandit:~$ ls
readme
![Explain Shell: LS Command](../../assets/images/overthewire/bandit/bandit0/bandit0_ls.png)

What's happening:

ls lists all files in the current directory

We found a file called readme

Step 3: Read the File
bash
bandit0@bandit:~$ cat readme
![Explain Shell: CAT Command](../../assets/images/overthewire/bandit/bandit0/bandit0_cat-readme.png)

Output:

text
The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
What's happening:

cat displays the contents of the file

The password is inside!

🎯 Password for Next Level
text
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
📚 Lessons Learned
Concept	What I Learned
SSH Basics	Remote connections using ssh with custom ports (-p)
File Navigation	ls to list files in the current directory
File Reading	cat to view file contents
➡️ What's Next
Level 1 → (Coming soon!)

First level complete! On to the next one... 