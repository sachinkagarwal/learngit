Experimenting with Git
======================

This is an experiment with Git.

## Experiment 1
Creating a branch
```
git checkout -b feature/TKT-2
```
Creating a new remote branch that the new local branch can track
```
git push -u <remote> feature/TKT-2
#To list the remote names run "git remote -vv", it is usually "origin" if not specified"
```

## Experiment 2
Merging a change into another branch
* First, commit any work on the branch you are working on.
  For example, on branch feature/TKT-2
  ```
  git commit -a -m "Implemented feature described in ticket TKT-2"
  ```
* Next, checkout the branch you want to merge the changes of feature/TKT-2 and run a merge command.
  ```
  git checkout master
  git pull
  git merge feature/TKT-2
  ```
  Usually, the master branch may have commits from other developers, thats why its a good idea to run git pull before running the merge. If this does not apply to you then the "git pull" command can be omitted.

  When you merge there may be 2 outcomes
  1. Git is able to do an automatic merge, in which case the changes from feature/TKT-2 should now reflect in the corresponding files of the master branch in the example above.
  2. Git was unable to merge the changes automatically because of conflicts (usually meaning that the same lines were edited differently on the branches being merged).

## Experiment 3
Conflict Resolution

Here is a master branch with a conflict.
 

