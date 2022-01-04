# GIT LABs task 1:
## Conflicts:
## Clone repo: https://github.com/csuvikg/tap-git
## Create file name.txt, containing your name
## Merge add-name branch
## Push your changes to a new branch

### Execution

```bash
git clone https://github.com/csuvikg/tap-git

cd tap-git

echo "Georgi Fuchedzhiev" > name.txt

git add name.txt

git commit -m "Added my name to name.txt in main branch."

git merge origin/add-name

Edited name.txt file and left only my name.

git add name. txt

git commit -m "Resolved conflict in name.txt, while merging origin/add-name to origin/main branch."

git checkout -b gf-git-labs-task-1-branch

git push --set-upstream origin gf-git-labs-task-1-branch
```

### Git log state:

```bash
commit ab2799dffefa65fdb26ccb1717a8484d8b9ea43a
Merge: df68d33 eccf2c9
Author: Georgi Fuchedzhiev <georgifuchedzhiev@infinitelambda.com>
Date:   Tue Jan 4 14:26:23 2022 +0200

    Resolved conflict in name.txt, while merging origin/add-name to origin/main branch.

commit df68d332ab223ab957fc7d29eeb4cf97e44dffe7
Author: Georgi Fuchedzhiev <georgifuchedzhiev@infinitelambda.com>
Date:   Tue Jan 4 14:24:31 2022 +0200

    Added my name to name.txt in main branch.

commit eccf2c924dd49ee9367f435a81ed680bcf396e92
Author: Georgi Fuchedzhiev <georgifuchedzhiev@infinitelambda.com>
Date:   Tue Jan 4 13:41:46 2022 +0200

    Added my name in name.txt file.

commit 4472c6e6a4316991d0b4ad290fa7c0a78dba84ca
Author: csuvikg <gaborcsuvik@gmail.com>
Date:   Mon Jan 3 21:40:57 2022 +0100

    Add name.txt

commit c281ccea8a035a87aa0795b477ee50a6d739ce4a
Author: csuvikg <gaborcsuvik@gmail.com>
Date:   Mon Jan 3 21:38:47 2022 +0100

    Add readme
```
Commit eccf2c924dd49ee9367f435a81ed680bcf396e92 added by mistake.
