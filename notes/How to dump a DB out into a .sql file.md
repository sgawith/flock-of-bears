# How to dump a DB out into a .sql file
Use the pg_dump command, specifying your access credentials, the database name and the target filename.

` pg_dump -U <username> -h <host name> <db name> > ~/Desktop/dump.sql`

Source: [postgresql.org](https://www.postgresql.org/docs/9.6/static/app-pgdump.html)

#postgres