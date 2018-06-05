# Removing .DS_Store files
Damn those .DS_Store files!

Here's how to recursively delete them from all descendent folders of the current folder.

`find . -name '*.DS_Store' -type f -delete`

#macos