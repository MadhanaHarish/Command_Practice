1. Created a empty git repo. ***git init***
2. Created a Readme.md file.
3. Checked ***git status***
---
No commits yet

Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file:   Readme.md

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified:   Readme.md

Untracked files:
(use "git add <file>..." to include in what will be committed)
.idea/
Git.iml
---
4. Staging unstaged file. ***git add Readme.md***
5. Checked ***git status***
---
On branch main

No commits yet

Changes to be committed:
(use "git rm --cached <file>..." to unstage)
new file:   Readme.md

Untracked files:
(use "git add <file>..." to include in what will be committed)
.idea/
Git.iml
---
6. Commiting to Local repo. ***git commit -m "First commit"***
7. Connecting global repo and pushing changes. 
---
git branch -M main\
git remote add origin https://github.com/MadhanaHarish/Command_Practice.git \
git push -u origin main
---
8. Errors faced.
---
madhana-nts0481:Git madhana-nts0481$ git push -u origin main\
Username for 'https://github.com': MadhanaHarish\
Password for 'https://MadhanaHarish@github.com':\
remote: Invalid username or token. Password authentication is not supported for Git operations.
fatal: Authentication failed for 'https://github.com/MadhanaHarish/Command_Practice.git/'

**SOLUTION**\
github -> settings -> developer setting -> generate personal access token -> generate new token.\
Generate and use the token insted of password. Then,

madhana-nts0481:Git madhana-nts0481$ git push -u origin main\
Username for 'https://github.com': MadhanaHarish\
Password for 'https://MadhanaHarish@github.com':\
Enumerating objects: 3, done.\
Counting objects: 100% (3/3), done.\
Delta compression using up to 12 threads\
Compressing objects: 100% (2/2), done.\
Writing objects: 100% (3/3), 497 bytes | 497.00 KiB/s, done.\
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)\
To https://github.com/MadhanaHarish/Command_Practice.git \
\* [new branch]      main -> main\
  branch 'main' set up to track 'origin/main'.
---
9. Using **rm** and **reset**.
---
* Creating a rough file named **dele.txt**.(Untracked files: dele.txt)
* Stage it using **git add dele.txt**.(Changes to be committed: new file:   dele.txt)
* Unstage it using **git reset dele.txt**.(Untracked files: dele.txt)
* Re-Stage using **git add dele.txt**.(NOTE: rm works on only tracked files)
* Commit using **git commit -m "adding dele.txt"**.
* Push it **git push**.(NOTE: rm works even after commiting)
* Remove using **git rm dele.txt**.(NOTE: after rm you need to commit changes and push it to global repo to see the changes).
---