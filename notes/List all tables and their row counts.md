# List all tables and their row counts
To list all tables in a PostgreSQL schema, with their row counts, use the following query. Note that the row counts seem to be highly suspect - quite a few populated tables were listed as having 0 rows.

```
select n.nspname as table_schema,
       c.relname as table_name,
       c.reltuples as rows
from pg_class c
join pg_namespace n on n.oid = c.relnamespace
where c.relkind = 'r'
      and n.nspname not in ('information_schema','pg_catalog')
order by c.reltuples desc;
```

Source: [dataedo.com](https://dataedo.com/kb/query/postgresql/list-of-tables-by-the-number-of-rows)

#sql #postgres