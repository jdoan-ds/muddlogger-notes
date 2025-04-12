# 🐙 Git & GitHub Cheat Sheet

Because version control should not feel like a wizard duel. Here's a clean, no-BS guide to Git and GitHub commands you'll actually use.

---

## 🔧 Basic Git Setup (One-Time)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## 📁 Starting a Local Repo

```bash
cd project-folder/
git init                      # start repo
git add .                     # stage all files
git commit -m "Initial commit"  # first commit
```

---

## 🔗 Connect to GitHub

```bash
git remote add origin https://github.com/username/repo-name.git
git branch -M main
git push -u origin main
```

---

## 🚀 Everyday Commands

| Action              | Command                            |
|---------------------|-------------------------------------|
| Check status        | `git status`                        |
| Add a file          | `git add filename.py`               |
| Add all files       | `git add .`                         |
| Commit changes      | `git commit -m "Your message"`      |
| Push to GitHub      | `git push`                          |
| Pull from GitHub    | `git pull`                          |
| View commit history | `git log`                           |

---

## 🌿 Branching Basics

```bash
git checkout -b feature-name   # create + switch

git switch main                # go back to main
git merge feature-name         # merge feature into main
```

---

## 🔄 Sync Your Repo

```bash
git pull origin main           # pull latest
```

---

## 🔍 Inspect and Undo

```bash
git diff                       # see changes

git checkout filename.py       # discard local changes

git reset HEAD~1               # undo last commit (local only)
```

---

## 🧠 Tips

- Always pull before you push
- Use short, clear commit messages
- Branch before experiments
- Don’t fear the merge — fear not committing often

---

## 📘 Resources

- git-scm.com – Official Git Book
- GitHub Docs
- ohmygit.org – Interactive Git learning game

---