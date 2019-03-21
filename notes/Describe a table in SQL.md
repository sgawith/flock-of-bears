# Describe a table in SQL
To get a list of columns in a table in a SQL query:

```
SELECT
 COLUMN_NAME
FROM
 information_schema.COLUMNS
WHERE
 TABLE_NAME = 'city';
```

Source: [postgrestutorial.com](http://www.postgresqltutorial.com/postgresql-describe-table/)

 #sql #postgres