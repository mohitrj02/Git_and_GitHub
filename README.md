# Git & GitHub

## 📌 What is GitHub?
GitHub is a cloud-based platform where developers store and manage their code using Git.

### Why GitHub?
- Backup your code online
- Collaborate with others
- Track project history
- Work from anywhere

---

## 📌 What is Git?
Git is a Version Control System (VCS).

### Why Git?
- Tracks changes in code
- Helps revert mistakes
- Enables teamwork without conflicts
- Maintains history of project

---

## 📌 Key Concepts

### 🔹 Repository (Repo)
A folder where your project files and history are stored.

### 🔹 Local vs Remote
- Local → Your system
- Remote → GitHub

---

## 📌 Setting Up Git

### Install Git & Check:
```bash
git --version
```

### Configure Git:
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list
```

👉 This tells Git who is making changes (important for tracking).

---

## 📌 Basic Terminal Commands

```bash
ls      # list files
pwd     # current directory
cd      # change directory
cd..    # change to back directory
mkdir directory_name  # create folder
git log # log of all the commits
clear   # clear terminal
q       # when used 'git log' then to go back we can write "q"
```

👉 These help navigate your system.

---

## 📌 Git Workflow (Most Important)

👉 FLOW:
GitHub → Clone → Modify → Add → Commit → Push

### Explanation:
1. Clone → copy project locally
2. Modify → make changes
3. Add → stage changes
4. Commit → save changes
5. Push → upload to GitHub

---

## 📌 Clone Repository

```bash
git clone <repo_link>
```

👉 Why?
To bring existing project from GitHub to your system.

---

## 📌 Git Status

```bash
git status
```

👉 Why?
To check current state of files.

---

## 📌 File States Explained

- Untracked → new files that git doesn't track yet
- Modified → file changed
- Staged → ready to commit
- Unmodified → no changes / unchanged

👉 Understanding this is VERY IMPORTANT.

---

## 📌 Add Command

```bash
git add file_name   # for single file
git add .           # for multiple files
```

👉 Why?
Moves files to staging area (preparing for commit).

---

## 📌 Commit Command

```bash
git commit -m "message"
```

👉 Why?
Creates a snapshot of your changes.

---

## 📌 Push Command

```bash
git push origin main
```

👉 Why?
Uploads your commits to GitHub.

---

## 📌 Init (Starting Project Locally)

```bash
git init
```

👉 Why?
Converts a normal folder into Git repository.

---

## 📌 Connect to GitHub

```bash
git remote add origin <repo-link>
git push -u origin main
```

👉 Why?
Links your local repo with GitHub.

---

## 📌 Branching (Very Important)

```bash
git branch                      # current working branch
git branch -M main              # rename branch
git checkout -b new_branch      # create new branch
git checkout branch_name        # to navigate
git branch -d branch_name       # to delete branch (always checkout from the branch to delete it)
```

👉 Why?
Work on features without affecting main code.

---

## 📌 Merge

```bash
way 1 :
git diff branch_name    # compare commits, branches, files & more
git merge branch_name   # merge 2 branches

way 2 :
Create PR
```

👉 Why?
Combine code from different branches.

---

## 📌 Pull Request (PR)

👉 Used on GitHub to merge changes.

Flow:
PR → Review → Merge

---

## 📌 Pull Command

```bash
git pull origin main
```

👉 Why?
Sync your local repo with GitHub.

---

## 📌 Merge Conflicts

👉 Happens when same file edited in multiple branches.

### Fix:
- Edit file manually
- Remove conflict markers
- Commit again

```bash
- Remove the unwanted lines that VS Code has create i.e <<<<<HEAD, ====, >>>>MAIN
- Now, keep the features you wanted and remove the unwanted features or, keep both the features
- Save the file. Then check git status -> git add . -> git commit -m "msg" -> git status
- Now, "nothing to commit" will appear. Check git diff main, so we have 1 extra change with comparison to 'main'
- Go to main branch using git checkout main, and now git merge <-branch_name->
- Now, the changes can automatically be merged.
- Push the changes to the remote repo using git push.
```

---

## 📌 Undo Changes

### Reset staged:staged changes (which are added but not commited)
```bash
git reset
```

### Undo commit: commited changes (for one commit)
```bash
git reset HEAD~1
```
### Undo multi commit: commited changes (for many commits)
```bash
git reset commit_hash
git reset --hard commit_hash
```
#### Hash is basically the 'code' for a perticular 'commit'. Which we can easily get using the 'git log' and we gets log of commit with their details

---

## 📌 Fork

👉 Copy someone else's repo to your GitHub.

### Why?
To contribute to open source projects.

```bash
- search for the repository you wanted to fork
- "fork" option is present on the right side of the GitHub, click that
- gets option to rename the repository for your account.
- save and get the repository in your account.
```

---

## 📌 Summary (Must Remember)

- Git = Version Control
- GitHub = Cloud storage for code
- Commit = Save point
- Push = Upload
- Pull = Download updates
- Branch = Work separately

---

## 🎯 Final Tip
Always follow:
👉 Pull → Work → Add → Commit → Push

This avoids conflicts and errors.
