# Getting the next available id from a table
If you're not using auto_increment, but you are using integer IDs, you'll probably need to get (and allocate) the next available ID in the sequence at some point, and you want to do it in the most atomic way possible.

Here was my first effort:

```
DECLARE sequenceNumber INT DEFAULT 0;
SELECT 1 + id INTO sequenceNumber FROM Seq ORDER BY id DESC LIMIT 1;
INSERT INTO Seq VALUES(sequenceNumber);
RETURN sequenceNumber;
```

And here's what Chris Palmer showed me. Nice! (but baffling).

```
DECLARE sequenceNumber INT DEFAULT 0;
UPDATE Seq SET id=last_insert_id (id + 1);
SELECT last_insert_id() INTO sequenceNumber;
RETURN sequenceNumber;
```

It's all about the last_insert_id voodoo! Isn't it nice, though? The read and write happen on the same line, so they're atomic and thread-safe.

#sql #mysql