# Counting open file handles for a process
In linux, the maximum number of open file handles per process is, by default, set to 1024.

As well as opening actual files on disk, other activities such as opening http or JMS connections also require file handles, which contribute towards the use of the limit.

This command will give you a count of the open files for the a java process:

```
pidof java | awk '{print "lsof -a -p "$1" | wc -l"}' | sh
```

The downside of this combined command is that it only really works if you're running only a single java process. If you have multiple processes, it's hard to know which one will be reported upon. The combined command is using 5 different commands, so let's break it down.

## Getting the pid of the process
```
pidof java
```

This lists (space-separated) the pids of all the running java processes. If you have multiple processes running, it might be more useful to view them in detail:

```
ps -aef | grep java
```

## Extracting the pid and using it as part of a command
```
awk '{print "..."$1"..."}'
```

Using awk, we extract the first column from the output of pidof ($1) and construct it into a new bash command.

## Getting a list of open file handles for the process
```
lsof -a -p 123456
```

The command lsof lists open file handles. Using the argument -p , we can limit it to file handles belonging to the specified process.

## Counting the entries in the list
```
wc -l
```

wc, or word count, counts the words in the specified content. In this case, it's piped from lsof, and it's using the -l qualifier, so it's counting lines.

## Executing the constructed command
```
sh
```

By piping the output of the awk command (which constructs a new bash command in string form) into sh, we can execute the new command.

#java #linux #awk