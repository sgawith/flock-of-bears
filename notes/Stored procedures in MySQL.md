# Stored procedures in MySQL
Stored procedures are tasty little snippets that you can use to safely run queries on your DB.

Here's a simple one to increment the highest number in a table and return the new value (like auto_increment, but not vulnerable to restores / data migrations).

```
DROP FUNCTION `GetNextSeq`;
CREATE DEFINER=`root`@`localhost` FUNCTION `GetNextSeq`() RETURNS INT(11) NOT DETERMINISTIC MODIFIES SQL DATA SQL SECURITY DEFINER BEGIN
	DECLARE sequenceNumber INT DEFAULT 0;
	SELECT 1 + id INTO sequenceNumber FROM Seq ORDER BY id DESC 	LIMIT 1;
	INSERT INTO Seq VALUES(sequenceNumber);
	RETURN sequenceNumber;
END 
```

That's clearly a pretty basic example, but it's nice enough for now.

Sources:
* [mysqltutorial.org](http://www.mysqltutorial.org/getting-started-with-mysql-stored-procedures.aspx)
* [stackoverflow.com](https://stackoverflow.com/questions/15935467/how-to-create-unique-sequence-in-mysql)

#sql #mysql