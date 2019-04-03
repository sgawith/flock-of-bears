# Deleting a branch in git
First, list the local branches:

`git branch`

To delete a **local** branch:

`git branch -d <branch name>`

If the branch isn't fully merged, you'll see a warning. To delete a branch even though it has pending commits:

`git branch -D <branch name>`

To delete a **remote** branch:
`git push origin :<branch name>`

Pruning your local “cache” of remote branches:

Sometimes the git cache becomes out of sync. This command fetches updates from the remote

`git fetch -p origin`

Source: [git-scm.com](https://git-scm.com/book/en/v2/Git-Branching-Branch-Management)

#git