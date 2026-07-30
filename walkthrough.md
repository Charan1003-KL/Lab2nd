# Git Walkthrough: Push, Fetch, Merge, Pull, and Reset

This walkthrough details the basic Git commands used to perform **Push**, **Fetch**, **Merge**, **Pull**, and **Reset** operations on a GitHub repository.

---

## 1. Initial Setup

Before using Git commands, configure your name and email:

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

---

## 2. Git Push

The `git push` command uploads your local branch commits to the remote repository.

### Commands:
```bash
# 1. Stage your changes (add files to the staging area)
git add walkthrough.md

# 2. Commit the staged changes with a descriptive message
git commit -m "Add walkthrough file documenting Git commands"

# 3. Push the local commits to the remote repository (origin) on the main branch
git push origin main
```

---

## 3. Git Fetch

The `git fetch` command downloads commits, files, and references from the remote repository to your local machine, but does **not** merge them into your working files.

### Commands:
```bash
# Fetch updates from the remote repository (origin)
git fetch origin
```

---

## 4. Git Merge

The `git merge` command integrates changes from another branch (such as a remote tracking branch) into your current active local branch.

### Commands:
```bash
# Merge remote changes into your local main branch after fetching
git merge origin/main
```

---

## 5. Git Pull

The `git pull` command is a combination of `git fetch` and `git merge` in a single step. It downloads remote changes and integrates them directly.

### Commands:
```bash
# Fetch and merge changes from the remote repository (origin) in one step
git pull origin main
```

---

## 6. Git Reset

The `git reset` command moves the current branch head to a specified commit, allowing you to undo changes.

### Commands:
```bash
# Undo the last commit, but keep the changes in your working directory (unstaged)
git reset HEAD~1

# Undo the last commit and completely discard all changes (destructive)
git reset --hard HEAD~1
```
