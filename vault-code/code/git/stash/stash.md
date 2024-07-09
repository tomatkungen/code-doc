```shell
# list stash list
git stash list

# list stash "git stash list <show total>" recent
git stash list -3

# list stash diffs
git stash list -p

# list stash concise
git stash list --oneline
```

```shell
# Remove only the first stash
git stash drop 

# Remove all in the stash list 
git stash clear
```

```shell
# Keep in the stash and copy file unstaged in directory
git stash apply

# Removes from stash to unstaged files in  directory
git stash pop
```

![[Screenshot 2024-07-09 at 12.30.47.png]]