---
layout: default
title: "Bandit Level 2"
---

# Bandit Level 2

## Goal

Find the password for Level 3 in a file whose name contains spaces.

## Commands used

- `ssh`
- `ls`
- `cat`

## Solution

### 1. Connect to the server

```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
```

### 2. Inspect the directory

```bash
ls
```

The file is named `--spaces in this filename--`, which contains spaces.

![SSH session](/assets/images/overthewire/bandit/bandit2/bandit2_ssh.png)

![Directory listing](/assets/images/overthewire/bandit/bandit2/bandit2_ls.png)

### 3. Read the file correctly

```bash
cat "--spaces in this filename--"
```

The password is:

```text
7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
```

![File content](/assets/images/overthewire/bandit/bandit2/bandit2_cat.png)

## Key learning

Files with spaces in their names must be quoted so the shell treats them as a single argument.