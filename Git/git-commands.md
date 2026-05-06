# Git Commands Cheat Sheet

## 1. Initialize Repository

```bash
git init
```

---

## 2. Add Files to Staging Area

Add specific file:

```bash
git add filename
```

Add all files:

```bash
git add .
```

---

## 3. Commit Changes

```bash
git commit -m "Commit message"
```

---

## 4. Push Changes to GitHub

```bash
git push origin main
```

First push:

```bash
git push -u origin main
```

---

## 5. Pull Changes from GitHub

```bash
git pull origin main
```

---

## 6. Configure Username and Email

```bash
git config --global user.name "Your Name"

git config --global user.email "your_email@example.com"
```

---

## 7. Clone Repository

```bash
git clone repository_url
```

Example:

```bash
git clone https://github.com/user/repo.git
```

---

## 8. Create Branch

```bash
git branch branch_name
```

---

## 9. Switch Branch

```bash
git checkout branch_name
```

Modern command:

```bash
git switch branch_name
```

---

## 10. Create and Switch Branch

```bash
git checkout -b branch_name
```

Modern command:

```bash
git switch -c branch_name
```

---

## 11. Merge Branch with Main

```bash
git checkout main

git merge branch_name
```

---

## 12. Check Repository Status

```bash
git status
```

---

## 13. View Commit History

```bash
git log
```

Compact version:

```bash
git log --oneline
```

---

## 14. View Branches

```bash
git branch
```

---

## 15. Remove File from Staging Area

```bash
git restore --staged filename
```

---

## 16. Restore File Changes

```bash
git restore filename
```

---

## 17. Add Remote Repository

```bash
git remote add origin repository_url
```

Check remotes:

```bash
git remote -v
```

---

# Git Workflow

```text
Working Directory
       ↓
   git add
       ↓
 Staging Area
       ↓
  git commit
       ↓
 Local Repository
       ↓
   git push
       ↓
 Remote Repository
```