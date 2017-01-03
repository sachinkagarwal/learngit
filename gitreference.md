# Useful git commands.

## Credentials

Caching Credentials
```
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=3600'
```

##Logging commands
Viewing history graph
```
git log --pretty=oneline --abbrev-commit  --graph
```
Git command history 
```


# Show local commands 
git reflog
# Show local commands yesterday
git show master@{yesterday}
# Details of the reflog
git log -g master
```
## Branch commands
Get list of all branches on remote
```
git branch -a
```

Look at a remote's information; this also shows tracking information
```
git remote show <remote-name e.g. origin>
```

Create a branch and set it to track a remote branch
```
git checkout -b <new-branch> remotes/<remote-name>/branch-to-track
# the remote branch name can be read off from the output of git branch -a
```

Show commit corresponding to branch
git rev-parse <branch-name>


### Merge related commands
Show which branches have been merged (or not merged). Merged branches can be deleted.
``` 
git branch --merged
git branch --no-merged
```

Deleting a (merged) branch; this doesn't work if the branch is not merged, in which case you need to use a force delete switch (-D)
```
git branch -d <branchname>
```

### Undoing changes

This is a good description
https://www.atlassian.com/git/tutorials/undoing-changes

Gist: revert and reset and clean

Also look at rebase and reflog here

https://www.atlassian.com/git/tutorials/rewriting-history

(particularly interactive rebase to remove too many commits)



