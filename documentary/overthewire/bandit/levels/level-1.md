---

#### `documentary/overthewire/bandit/levels/level-1.md`

```markdown
---
layout: default
title: "Bandit Level 1"
---

# $ Bandit Level 1

---

## 📋 Level Information

| Property | Value |
|----------|-------|
| **Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Username** | `bandit1` |
| **Password** | `6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR` |
| **Goal** | Find the password for Level 2 in a file called `-` |

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
ssh bandit1@bandit.labs.overthewire.org -p 2220
Password: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

💡 Tip: Notice the file is named - — that's unusual!

https:///assests/images/overthewire/bandit/bandit1/bandit1_ssh.png

Step 2: Explore the Directory
bash
bandit1@bandit:~$ ls
-
We found a file called - (just a dash). This is tricky because - is a special character in Linux.

https:///assests/images/overthewire/bandit/bandit1/bandit1_ls.png

Step 3: Read the File
bash
bandit1@bandit:~$ cat ./-
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
Why ./-?

cat - would read from standard input (keyboard), not a file

./- tells Linux "look in the current directory for a file named -"

https:///assests/images/overthewire/bandit/bandit1/bandit1_cat-dash.png

🎯 Password for Next Level
text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
📚 Key Learnings
Concept	What I Learned
Special Filenames	Files can have names like - that need special handling
Current Directory	./ specifies the current directory
➡️ Next Level
Level 2 →

The file named - taught me that filenames matter in Linux.