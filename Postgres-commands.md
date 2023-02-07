## Useful Postgres Commands

-l: psql will list all databases and then exit (useful if the user you connect with doesn't has a default database, like at AWS RDS)
Most \d commands support additional param of __schema__.name__ and accept wildcards like *.*
\?: Show help (list of available commands with an explanation)
\q: Quit/Exit
\c __database__: Connect to a database
\d __table__: Show table definition (columns, etc.) including triggers
\d+ __table__: More detailed table definition including description and physical disk size
\l: List databases
\dy: List events
\df: List functions
\di: List indexes
\dn: List schemas
\dt *.*: List tables from all schemas (if *.* is omitted will only show SEARCH_PATH ones)
\dT+: List all data types
\dv: List views
\dx: List all extensions installed
\df+ __function__ : Show function SQL code.
\x: Pretty-format query results instead of the not-so-useful ASCII tables
\copy (SELECT * FROM __table_name__) TO 'file_path_and_name.csv' WITH CSV: Export a table as CSV
\des+: List all foreign servers
\dE[S+]: List all foreign tables
\! __bash_command__: execute __bash_command__ (e.g. \! ls)
