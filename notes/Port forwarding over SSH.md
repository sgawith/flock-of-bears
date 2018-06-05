# Port forwarding over SSH
If a remote port isn't open publicly, but you are able to SSH to the server, you can expose the port over your SSH connection to use local apps.

`ssh -L <local port>:<target host name:<remote port> <ssh target>`

e.g.

`ssh -L 3306:127.0.0.1:3306 my.awesome.db.host`

#ssh