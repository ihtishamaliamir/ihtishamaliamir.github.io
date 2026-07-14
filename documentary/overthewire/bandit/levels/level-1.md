---
layout: default
title: "Bandit Level 1"
---

# Bandit Level 1

## Goal

Find the password for Level 2 in a file named `-`.

## Commands used

- `ssh`
- `ls`
- `cat`

## Solution

### 1. Connect to the server

```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

### 2. Inspect the directory

```bash
ls
```

The file is named `-`, so a normal `cat -` would try to read from standard input instead of the file.

![SSH session](/assets/images/overthewire/bandit/bandit1/bandit1_ssh.png)

### 3. Read the target file

```bash
cat ./-
```

The password is:

```text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

![Directory listing](/assets/images/overthewire/bandit/bandit1/bandit1_ls.png)

![Cat dash output](/assets/images/overthewire/bandit/bandit1/bandit1_cat-dash.png)

## Key learning

A filename like `-` needs special handling in the shell. Using `./-` tells Linux to read the file in the current directory rather than treating it as stdin.