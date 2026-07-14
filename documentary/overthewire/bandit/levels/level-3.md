---

#### `documentary/overthewire/bandit/levels/level-3.md`

```markdown
---
layout: default
title: "Bandit Level 3"
---

# $ Bandit Level 3

---

## 📋 Level Information

| Property | Value |
|----------|-------|
| **Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Username** | `bandit3` |
| **Password** | `7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME` |
| **Goal** | Find the password for Level 4 in a hidden file |

---

## 🔧 Commands Used

| Command | Purpose |
|---------|---------|
| `ssh` | Secure Shell — remote connection |
| `cd` | Change directory |
| `ls` | List files |
| `ls -la` | List ALL files (including hidden) |
| `cat` | Display file contents |

---

## 🔍 Solution

### Step 1: Connect to the Server

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
Password: 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

![SSH](../../../assests/images/overthewire/bandit/bandit3/bandit3_ssh.png)

Step 2: Explore the Directory
bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
![CD](../../../assests/images/overthewire/bandit/bandit3/bandit3_cd-inhere.png)

bash
bandit3@bandit:~/inhere$ ls
(nothing shows up)
![LS](../../../assests/images/overthewire/bandit/bandit3/bandit3_ls.png)

Why is nothing showing? The file is hidden!

Step 3: Find Hidden Files
bash
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Jun 24 14:59 .
drwxr-xr-x 3 root    root    4096 Jun 24 14:59 ..
-rw-r----- 1 bandit4 bandit3   33 Jun 24 14:59 ...Hiding-From-You
![LS -LA](../../../assests/images/overthewire/bandit/bandit3/bandit3_ls-la.png)

What does -la do?

-l = long format (shows permissions, owner, size)

-a = all files (including hidden ones)

Step 4: Read the Hidden File
bash
bandit3@bandit:~/inhere$ cat ./...Hiding-From-You
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
![CAT](../../../assests/images/overthewire/bandit/bandit3/bandit3_cat.png)

🎯 Password for Next Level
text
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
📚 Key Learnings
Concept	What I Learned
Hidden Files	Files starting with . are hidden
ls -la	Shows ALL files including hidden ones
➡️ Next Level
Level 4 →

Hidden files taught me that not everything is visible at first glance.