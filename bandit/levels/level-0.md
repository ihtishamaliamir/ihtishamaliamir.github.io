---
layout: default
title: "Bandit Level 0"
parent: "Bandit"
---

# 🎮 Bandit Level 0

## 📋 The Goal
Connect to the OverTheWire server using SSH and retrieve the password for Level 1.

**Level Info:**
- **Host:** `bandit.labs.overthewire.org`
- **Port:** `2220`
- **Username:** `bandit0`
- **Password:** `bandit0`

---

## 🔧 The Command

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
https://../assets/images/overthewire/bandit/bandit0/bandit0_ssh.png

Breaking It Down
Part	Meaning
ssh	Secure Shell client — used for secure remote connections
bandit0@	The username for this level
bandit.labs.overthewire.org	The server hostname
-p 2220	Port number (SSH defaults to 22, but this server uses 2220)
🔍 Walkthrough
Step 1: Connect to the Server
bash
┌──(kiddo㉿Machine)-[~]
└─$ ssh bandit0@bandit.labs.overthewire.org -p 2220
What happens next:

You'll see the OverTheWire banner

You'll be prompted for a password

text
bandit0@bandit.labs.overthewire.org's password: bandit0
💡 Tip: When typing the password, nothing will appear on screen — this is normal for security!

Step 2: Explore the Directory
Once logged in, let's see what files are available:

bash
bandit0@bandit:~$ ls
readme
https://../assets/images/overthewire/bandit/bandit0/bandit0_ls.png

📌 Key Learning: ls lists all files in the current directory. We found a file called readme — this likely contains the password!

Step 3: Read the File
bash
bandit0@bandit:~$ cat readme
https://../assets/images/overthewire/bandit/bandit0/bandit0_cat-readme.png

Output:

text
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/

The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
📌 Key Learning: cat displays the contents of a file.

🎯 Password Found
text
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
📚 Lessons Learned
Concept	What I Learned
SSH Basics	Remote connections using ssh with custom ports (-p)
File Navigation	ls to list files in the current directory
File Reading	cat to view file contents
Linux Structure	Home directory contains user-specific files
💡 Pro Tips
Always check for README or readme files — they often contain important info

SSH uses port 22 by default — if it's not working, check if a custom port is specified

Passwords are case-sensitive — copy them exactly!

Nothing appears when typing passwords — this is a security feature

🔗 Helpful Resources
Explain Shell: ssh command

SSH Manual

OverTheWire Bandit Page

➡️ What's Next
Use the password to connect to Level 1:

bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
Password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
First level complete! On to the next one... 🚀