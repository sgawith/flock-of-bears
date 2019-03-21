# How to clear out local references to remote branches
When you do a git pull, you get a list of remote branches. That will build up over time, even as remote branches are removed. To clear out all the ones which are no longer relevant:

`git remote update origin --prune`

#git