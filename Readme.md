Here is your content converted into a clean **README.md format** 👇

---

# Git Basic Workflow

## 1. Initialize a Git Repository

```bash
git init
```

---

## 2. Create a File

Create a file named:

```
Readme.md
```

---

## 3. Check Git Status

```bash
git status
```

Output:

```
No commits yet

Changes to be committed:
  new file:   Readme.md

Changes not staged for commit:
  modified:   Readme.md

Untracked files:
  .idea/
  Git.iml
```

---

## 4. Stage the File

```bash
git add Readme.md
```

---

## 5. Check Status Again

```bash
git status
```

```
On branch main

No commits yet

Changes to be committed:
  new file:   Readme.md

Untracked files:
  .idea/
  Git.iml
```

---

## 6. Commit to Local Repository

```bash
git commit -m "First commit"
```

---

## 7. Connect to Remote Repository & Push

```bash
git branch -M main
git remote add origin https://github.com/MadhanaHarish/Command_Practice.git
git push -u origin main
```

---

## 8. Error Faced (Authentication Issue)

```bash
Username for 'https://github.com': MadhanaHarish
Password for 'https://MadhanaHarish@github.com':
remote: Invalid username or token.
Password authentication is not supported for Git operations.
fatal: Authentication failed
```

---

## 9. Solution (Using Personal Access Token)

Steps:

1. Go to GitHub → **Settings**
2. Open **Developer settings**
3. Click **Personal access tokens**
4. Generate a new token
5. Copy the token

Then push again:

```bash
git push -u origin main
```

Use:

* **Username** → GitHub username
* **Password** → Paste the token

---

## Successful Push Output

```
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), done.
To https://github.com/MadhanaHarish/Command_Practice.git
 * [new branch] main -> main
branch 'main' set up to track 'origin/main'.
```

---

## 10. Understanding `git reset` and `git rm`

## Create a File

```
dele.txt
```

---

## Stage the File

```bash
git add dele.txt
```

```
Changes to be committed:
  new file: dele.txt
```

---

## Unstage the File

```bash
git reset dele.txt
```

```
Untracked files:
  dele.txt
```

---

## Stage Again

```bash
git add dele.txt
```

---

## Commit the File

```bash
git commit -m "Add dele.txt"
```

---

## Push to Remote

```bash
git push
```

---

## Remove File Using Git

```bash
git rm dele.txt
```

---

## Commit Removal

```bash
git commit -m "Remove dele.txt"
```

---

## Push Changes

```bash
git push
```

---

# Key Concepts

| Command            | Purpose                              |
| ------------------ | ------------------------------------ |
| `git add`          | Stage changes                        |
| `git reset <file>` | Unstage changes                      |
| `git rm <file>`    | Remove tracked file + stage deletion |
| `git commit`       | Save to local repository             |
| `git push`         | Upload to remote repository          |

---

# Important Notes

* `git rm` works **only on tracked files**
* `rm file.txt` removes file only from system
* `git rm file.txt` removes from system + Git
* Always **commit after `git rm`** to reflect changes in repo

---

