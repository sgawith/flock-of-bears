# Heap dump for running Java process
To do a dump of the memory heap of a Java process:

`jmap -dump:format=b,file=myfile.bin <pid>`

The resulting .bin file can then be analysed using the Eclipse memory analyser: [eclipse.org](https://www.eclipse.org/mat/) or jvisualvm, which is part of the JDK.


Source: [stackoverflow.com](https://stackoverflow.com/questions/15130956/how-to-analyse-the-heap-dump-using-jmap-in-java)