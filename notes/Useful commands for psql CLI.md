# Useful commands for psql CLI
* Connect to a database: `\c <db name>`
* List schemas: `\dn`
* Quit: `\q`
* Show current user’s search path: `SHOW search_path;`
* Update current user’s search path: `SET search_path TO myschema,public;`
* List all databases: `\l`


Sources:
* [postgresql.org](https://www.postgresql.org/docs/current/static/ddl-schemas.html)
* [dba.stackexchange.com](https://dba.stackexchange.com/questions/40045/how-do-i-list-all-schemas-in-postgresql)
* [stackoverflow.com](https://stackoverflow.com/questions/3949876/how-to-switch-databases-in-psql)
* 
 
#postgres