# Useful git commands.

## Credentials

Caching Credentials
```
git config --global credential.helper cache
git config --global credential.helper 'cache --timeout=3600'
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
git checkout -b 
