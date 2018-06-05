# Copying a file remotely using scp
If you need to transfer files between your machine and a remote machine. but you don't have access to an FTP package (or for whatever reason the remote machine is hard to connect to through an FTP tool), scp is the best way to go.

Copy the file "foobar.txt" from a remote host to the local host

`scp <username>@<hostname>:<remote file> <local path> `

Copy the file "foobar.txt" from the local host to a remote host

`scp <local file> <username>@<hostname>:<remote path>` 

Source: [hypexr.org](http://www.hypexr.org/linux_scp_help.php)

#macos #ssh