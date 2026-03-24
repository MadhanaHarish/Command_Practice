````md
# Branch Management in Git

## Move Between Branches

### Switch branches
```bash
git switch <name>
````

or

```bash
git checkout <name>
```

---

### Create a branch

```bash
git switch -c <name>
```

or

```bash
git checkout -b <name>
```

---

### List branches

```bash
git branch
```

---

### List branches by most recently committed

```bash
git branch --sort=-committerdate
```

---

### Delete a branch

```bash
git branch -d <name>
```

---

### Force delete a branch

```bash
git branch -D <name>
```
