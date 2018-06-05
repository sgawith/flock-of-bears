# Resurrecting a Jenkins slave
Sometimes  Jenkins slaves go offline for reasons unknown. If that happens, the Jenkins process often just needs restarting.

## Mac slaves
If the slave is running on a Mac, the following commands will restart the process:

```
launchctl unload ~/Library/LaunchAgents/org.jenkins-slave.plist
launchctl load ~/Library/LaunchAgents/org.jenkins-slave.plist
```

#jenkins #macos