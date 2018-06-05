# Tagging in git
To list tags on the current repository:

`git tag -l`

To tag the current point on the repository:

`git tag -a <tag name> -m "<commit message"`

To tag a previous commit on the repository:

`git tag -a <tag name> <commit ID> -m "<commit message>"`

To push a tag to the remote

`git push origin <tag name>`

Source:  [git-scm.com](https://git-scm.com/book/en/v2/Git-Basics-Tagging)

#git