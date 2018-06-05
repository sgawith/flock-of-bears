# Resolving conflicts
When merging, you may find that there are conflicts in files which have been updated on your branch and the source branch. Use the status command to find out which files have conflicts:
`git status`

## Fix the conflict
Open the conflicting file(s) in your editor of choice (IntelliJ has a nice merge  tool for this). Find all the conflicting sections (delimited by >>>> ===== and <<<<<<), update to a single, ideal merged copy and save.

## Mark the conflict as resolved
To let git know that the conflict has been resolved and the file is ready to commit, just add it.

`git add <your file>`

Your conflicts are resolved and you're ready to commit!

#git