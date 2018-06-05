# Removing an installed package
To remove a package, you may first wish to check which version is installed:

`apt-cache policy <package name>`

To then remove a package, use the following command:

`apt-get remove <package name>`

You can also remove using the dpkg command, if preferred:

`dpk --purge <package name>`

#linux #apt #dpkg