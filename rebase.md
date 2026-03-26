# Git Rebase & Related Concepts (Complete Guide)

---

## 1. What is Rebase?

Rebase is used to **move your branch on top of another branch**.

```bash
git rebase main
```

 It takes your commits and replays them on top of `main`.

---

## Example

### Before Rebase

```
main:    A --- B --- C
Branch:        \--- D --- E
```

### After Rebase

```
main:    A --- B --- C
Branch:                D' --- E'
```

 Only **Branch changes**, main remains same.

---

##  Purpose of Rebase

* Sync feature branch with latest main
* Resolve conflicts early
* Keep clean linear history

---

##  Important Rule

 Rebase updates **your branch**, not main.

---

## Rebase Workflow

```bash
git switch Branch
git rebase main

# fix conflicts if any

git switch main
git merge Branch
```

---

## ⚡ 2. Merge vs Rebase

| Feature  | Merge              | Rebase          |
| -------- | ------------------ | --------------- |
| History  | Branching          | Linear          |
| Commit   | Extra merge commit | No extra commit |
| Conflict | During merge       | During rebase   |

 Use rebase for clean history
 Use merge for safe integration

---

## 3. Fast-Forward Merge

After rebase:

```bash
git merge Branch
```

 No new commit created
 Just pointer moves forward

---

## 4. Cherry-Pick

Used to copy specific commit:

```bash
git cherry-pick <commit-id>
```

 Copies commit from one branch to another

---

##  Skipped Commits in Rebase

```
skipped previously applied commit
```

 Means:

* Commit already exists (maybe cherry-picked)
* Git avoids duplication

---

##  5. Tracked vs Untracked

| Type      | Meaning               |
| --------- | --------------------- |
| Untracked | Git not tracking file |
| Tracked   | Git managing file     |

 Becomes tracked after:

```bash
git add file.txt
```

---

##  6. git commit -am

```bash
git commit -am "message"
```

 Adds + commits **only tracked files**
 Ignores new untracked files

---

## 7. Fetch vs Pull

| Command   | Meaning                |
| --------- | ---------------------- |
| git fetch | Gets changes, no merge |
| git pull  | Fetch + merge          |

---

## 8. origin/main Meaning

* `origin` → remote repo
* `main` → branch in remote

 `origin/main` = remote tracking branch

---

## 9. Complete Lifecycle

```
Working → Staging → Commit → Remote
```

Commands:

```bash
git add .
git commit -m "msg"
git push origin main
```

---

## Final Summary

* Rebase = bring main changes into your branch
* Merge = bring branch changes into main
* Cherry-pick = copy specific commit
* Fetch = download changes
* Pull = download + apply

---

## One-Line Memory

"Rebase to update yourself, merge to update main"
