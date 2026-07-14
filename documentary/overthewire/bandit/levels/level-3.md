---
layout: default
title: "Bandit Level 3"
---

# Bandit Level 3

## Goal

Find the password for Level 4 in a hidden file.

## Commands used

- `ssh`
- `cd`
- `ls`
- `ls -la`
- `cat`

## Solution

### 1. Connect to the server

```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
```

### 2. Enter the directory

```bash
ls
cd inhere/
```

The directory contains a hidden file, so a regular `ls` does not show it.

![SSH session](/assets/images/overthewire/bandit/bandit3/bandit3_ssh.png)

![Changed directory](/assets/images/overthewire/bandit/bandit3/bandit3_cd-inhere.png)

### 3. Show hidden files

```bash
ls -la
```

This exposes the hidden file `...Hiding-From-You`.

![Hidden file listing](/assets/images/overthewire/bandit/bandit3/bandit3_ls-la.png)

### 4. Read the hidden file

```bash
cat ./...Hiding-From-You
```

The password is:

```text
xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
```

![Hidden file content](/assets/images/overthewire/bandit/bandit3/bandit3_cat.png)

## Key learning

Files beginning with `.` are hidden by default. `ls -la` reveals them.