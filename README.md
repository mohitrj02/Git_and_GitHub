# Git & GitHub Notes

## GitHub
Website that allows developers to store and manage their code using Git. Stores in folders known as **repositories**.

### GitHub Account
- Create a new repository: `mohitrj-demo`
- Make your first commit

---

## Git
A **Version Control System (VCS)** that helps track changes in code.

### Features:
- Popular  
- Free & Open Source  
- Fast & Scalable  

---

## Setting up Git

### Tools:
- Visual Studio Code (VS Code)
- Windows: Git Bash

### Check installation:
```bash
git --version
```

---

## Configure Git

```bash
git config --global user.name "My Name"
git config --global user.email "someone@email.com"
git config --list
```

**Note:**
- Global → applies to entire system  
- Local → applies to a specific repo  

`~` refers to root directory.

---

## Basic Commands

```bash
git --version   # Check version
ls              # List files/folders
clear           # Clear terminal
pwd             # Current directory
cd              # Change directory
cd ..           # Go back
mkdir folder    # Create folder
git log         # Show commit history
q               # Exit git log
```

---

## Local vs Remote

- **Local** → Your laptop/PC  
- **Remote** → GitHub  

---

## Clone & Status

### Clone Repository:
```bash
git clone <repository-link>
```

### Check Status:
```bash
git status
```

### Steps:
1. Copy GitHub repo link  
2. Clone it using command git clone <repository-link>
3. Navigate into folder (`cd`)  
4. List files (`ls`)  

---

## View File

- Normal files → `ls`
- Hidden files → `ls -a`

---

## Git Workflow

Modify → Add → Commit

---

## File Status Types

- **Untracked** → New file  
- **Modified** → Changed  
- **Staged** → Ready to commit  
- **Unmodified** → No changes  

---

## Add & Commit

### Add files:
```bash
git add <file_name>
git add .
```

### Commit changes:
```bash
git commit -m "message"
```

**Note:** Only commits are recorded in Git.

---

## Push Command

Upload local changes to GitHub:

```bash
git push origin main
```

- `origin` → remote repo  
- `main` → branch  

---

## Init Commands (Creating Repo Locally)

```bash
git init
git remote add origin <link>
git remote -v
git branch
git branch -M main
git push origin main
```

---

## Upstream Setup

```bash
git push -u origin main
```

After this, you can simply use:
```bash
git push
```

---

## Workflow Summary

GitHub → Clone → Change → Add → Commit → Push

---

## Git Branches

```bash
git branch
git branch -M main
git checkout <branch_name>
git checkout -b <new_branch>
git branch -d <branch_name>
```

### Push branch:
```bash
git push origin <branch_name>
```

---

## Merging Code

### Method 1:
```bash
git diff <branch_name>
git merge <branch_name>
```

### Method 2:
- Create Pull Request (PR)

---

## Pull Request (PR)

Used to propose changes.

### Workflow:
PR → Review → Merge

---

## Pull Command

Fetch and update local repo:

```bash
git pull origin main
```

---

## Merge Conflicts

Occurs when Git cannot auto-merge changes.

### Steps to resolve:
1. Open file in VS Code  
2. Remove conflict markers:
   ```
   <<<<<<< HEAD
   =======
   >>>>>>> main
   ```
3. Keep desired code  
4. Save file  

Then:
```bash
git status
git add .
git commit -m "resolved conflict"
git push
```

---

## Undoing Changes

### Case 1: Staged (not committed)
```bash
git reset <file_name>
git reset
```

### Case 2: Last commit
```bash
git reset HEAD~1
```

### Case 3: Multiple commits
```bash
git reset <commit_hash>
git reset --hard <commit_hash>
```

---

## Fork

A fork is a copy of another repository.

### Steps:
1. Search repo on GitHub  
2. Click **Fork**  
3. Rename if needed  
4. Repository appears in your account  

---

## Key Notes

- Git tracks commits, not adds  
- Remote repo = GitHub  
- Local repo = Your system  
- Always pull before pushing in collaborative work  
