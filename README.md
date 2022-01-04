## Create file, commit and revert commit in seperate branch

```
$ git checkout -b krasy2-branch
$ echo "My name" > changes.md
$ git add changes.md 
$ git commit -m "creating changes.md"
$ git revert d68be2f
```

## Create new file

```
$ echo "changelog" > changelog.md
$ git add changelog.md 
$ git commit -m "creating changelog.md"
```

## Drop first creation and revert commits

```

$ git rebase -i HEAD~3

...
d d68be2f creating changes.md
d 89a79d8 Revert "creating changes.md"
pick bd19d66 creating changelog.md
...
```

## Push 

```
$ git add changelog.md 
$ git commit -m "commit after removing changes.md"
$ git push -u origin krasy2-branch
```
