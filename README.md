# My Git cheatsheet

## CHECKING OUT
```
git checkout <branchname>
git checkout -b <new branchname>
```
## BRANCHES
```
git branch #list of local branches
git branch -a #list of local and remote branches
git branch -v #verbose list of local branches
git branch -vv #very verbose list of local branches
```

## DELETING UNUSED LOCAL REPOS
### First prune remote branches:
```
git remote prune origin
```
### Then run:
```
git branch -vv | grep 'origin/.*: gone]' | awk '{print $1}' | xargs git branch -d #Use capital D for hard remove
git branch -vv | grep 'origin/.*: gone]' #This lists the branches that will be removed.
```

## REMOVE LOCAL COMMITS
```
git reset --hard origin/<branch_name>
```

## TAGGING
```
git tag --list
git tag --list | grep xxx
```
