---
layout: default
title: "Bandit Level 0"
---

# $ Bandit Level 0

---

## 📋 Level Information

| Property | Value |
|----------|-------|
| **Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Username** | `bandit0` |
| **Password** | `bandit0` |
| **Goal** | Connect via SSH and retrieve the password for Level 1 |

---

## 🔧 Commands Used

| Command | Purpose |
|---------|---------|
| `ssh` | Secure Shell — remote connection |
| `ls` | List files in current directory |
| `cat` | Display file contents |

---

## 🔍 Solution

### Step 1: Connect to the Server

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
Password: bandit0

💡 Tip: Read the level goal carefully first. Then read the manual if you don't know what a command does.

https://../../../../assests/images/overthewire/bandit/bandit0/bandit0_ssh.png

Step 2: Explore the Directory
bash
bandit0@bandit:~$ ls
readme
https://../../../../assests/images/overthewire/bandit/bandit0/bandit0_ls.png

Step 3: Read the File
bash
bandit0@bandit:~$ cat readme
Output:

text
The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
https://../../../../assests/images/overthewire/bandit/bandit0/bandit0_cat-readme.png

🎯 Password for Next Level
text
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
📚 Key Learnings
Concept	What I Learned
SSH Basics	Remote connection with ssh and custom ports (-p)
File Navigation	ls to list what's there
File Reading	cat to view file contents
<div style="display: flex; justify-content: space-between; margin-top: 30px;"> <span style="background: var(--bg-tertiary); color: var(--text-muted); padding: 10px 20px; border-radius: 6px; border: 1px solid var(--border);">⬅️ Previous: —</span> <a href="/documentary/overthewire/bandit/levels/level-1/" style="background: var(--accent); color: white; padding: 10px 20px; border-radius: 6px; text-decoration: none; font-weight: 600;">Next Level 1 →</a> </div>
This didn't feel like much when I first did it. But looking back — this was the first step.