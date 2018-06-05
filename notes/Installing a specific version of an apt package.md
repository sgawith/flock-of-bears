# Installing a specific version of an apt package
First, list the available versions:

`apt-cache policy <package name>`

Then install the version you want:

`apt-get install <package name>=<version number>`

To check that you've got he version you wanted:

`dpkg -s <package-name>`

Sources:
* [Stack Overflow](http://stackoverflow.com/questions/18885820/how-to-check-the-version-before-install-packages-using-apt-get)
* [Andrew Beacock](http://blog.andrewbeacock.com/2007/03/how-to-install-specific-version-of.html)
* [How-to Geek](https://www.howtogeek.com/howto/ubuntu/see-what-version-of-a-package-is-installed-on-ubuntu/)

#linux #apt #dpkg