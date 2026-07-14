---
layout: default
title: "Bandit Level 4"
---

# Bandit Level 4

## Goal

Find the password for Level 5 in a human-readable file.

## Commands used

- `ssh`
- `cd`
- `ls`
- `file`
- `cat`

## Solution

### 1. Connect to the server

```bash
ssh bandit4@bandit.labs.overthewire.org -p 2220
```

### 2. Inspect the directory

```bash
ls
cd inhere/
```

The directory contains several files named `-file00` through `-file09`.

![SSH session](/assets/images/overthewire/bandit/bandit4/bandit4_ssh.png)

![Changed directory](/assets/images/overthewire/bandit/bandit4/bandit4_cd-inhere.png)

### 3. Identify file types

```bash
file ./-*
```

One file is ASCII text and is the likely target.

![File type output](/assets/images/overthewire/bandit/bandit4/bandit4_file.png)

### 4. Read the human-readable file

```bash
cat ./-file07
```

The password is:

```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

![File contents](/assets/images/overthewire/bandit/bandit4/bandit4_cat.png)

## Key learning

The `file` command helps identify which files are likely to contain readable text before you open them.