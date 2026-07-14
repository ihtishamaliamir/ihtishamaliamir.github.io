---

#### `documentary/overthewire/bandit/levels/level-2.md`

```markdown
---
layout: default
title: "Bandit Level 2"
---

# $ Bandit Level 2

---

## 📋 Level Information

| Property | Value |
|----------|-------|
| **Host** | `bandit.labs.overthewire.org` |
| **Port** | `2220` |
| **Username** | `bandit2` |
| **Password** | `PK8fYLZg2hnHSz83plBL1iEPKdD3QToB` |
| **Goal** | Find the password for Level 3 in a file with spaces in its name |

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
ssh bandit2@bandit.labs.overthewire.org -p 2220
Password: PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

💡 Tip: Notice the file has spaces in its name!

https:///assests/images/overthewire/bandit/bandit2/bandit2_ssh.png

Step 2: Explore the Directory
bash
bandit2@bandit:~$ ls
--spaces in this filename--
https:///assests/images/overthewire/bandit/bandit2/bandit2_ls.png

Step 3: Read the File (Correct Way)
Use quotes:

bash
bandit2@bandit:~$ cat "--spaces in this filename--"
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
https:///assests/images/overthewire/bandit/bandit2/bandit2_cat.png

🎯 Password for Next Level
text
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
📚 Key Learnings
Concept	What I Learned
Spaces in Filenames	Need to quote filenames with spaces
Quoting	"filename with spaces" tells the shell it's one argument
➡️ Next Level
Level 3 →

Quoting is a fundamental skill in the shell.