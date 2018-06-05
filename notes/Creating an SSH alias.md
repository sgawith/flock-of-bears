# Creating an SSH alias
To set up an SSH alias, create a file called ~_.ssh_config. In that file, you cna define multiple SSH aliases in the following format:

Host <alias>
User <user name>
Port <port>
HostName <server name>

You can then automatically log into that server by typing the following:

`ssh <alias>`

Source: [lookherefirst.wordpress.com](https://lookherefirst.wordpress.com/2007/12/17/a-simple-ssh-config-file/)

#macos #ssh