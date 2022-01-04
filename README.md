# Git Labs task 2:
## Rewriting history:
## Make sure you work on this newly created branch that is only used by you
## Create a changes.md to record that you added your name, commit the change
## Revert the previous commit
## Create a changelog.md instead to record your changes, commit
## Drop the first create and the revert commit, leaving only the second create one
## Push your changes

### Execution:

```bash
git checkout -b gf-git-labs-task-2-branch

echo Georgi Fuchedzhiev > changes.md

git add changes.md 

git commit -m "Added my name in changes.md file."

git revert 941fd54

echo "Changes before editing commit's history: " >> changelog.md

git log >> changelog.md

git add changelog.md 

git commit -m "Added changelog.md to track changes in commit's history."

git rebase -i HEAD~3

git log >> changelog.md

vi changelog.md 

git add changelog.md 

git commit -m "Repository state after removing create and revert commit."
```

### Git log state:

```bash
commit dd515e630c00a527067ae1b842713808902f2d9e
Author: Georgi Fuchedzhiev <georgifuchedzhiev@infinitelambda.com>
Date:   Tue Jan 4 15:55:03 2022 +0200

    Repository state after removing create and revert commit.

commit 88eaeceb00d1a14fdd73067b57424095893223fd
Author: Georgi Fuchedzhiev <georgifuchedzhiev@infinitelambda.com>
Date:   Tue Jan 4 15:52:57 2022 +0200

    Added changelog.md to track changes in commit's history.

commit c281ccea8a035a87aa0795b477ee50a6d739ce4a
Author: csuvikg <gaborcsuvik@gmail.com>
Date:   Mon Jan 3 21:38:47 2022 +0100

    Add readme
```
