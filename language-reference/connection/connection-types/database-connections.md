# Database Connections

## Description

* Applications need physical database connection\(s\) in order to execute SQL commands.
* New connections can be obtained by calling any one of the following functions : [create\_oracle\_connection](../../built-in-functions/sodium-built-in-functions/database-related-functions/create_oracle_connection.md) or [create\_postgresql\_connection](../../built-in-functions/sodium-built-in-functions/database-related-functions/create_postgresql_connection.md) function.
* Applications can have more than one database connection at the same time.
* All connections must have a unique name called as "connection name".
* If "connection name" is not provided by developer in source code, "default" is used as a default "connection name". As an example this happens when A data block does not specify its connection name in [Form File](../../program-structure/form-file.md) \([connection-name property](../../tags/data-block/#data-block-name-property)\).

## See also

### ["connection\_not\_found" trigger](../../built-in-triggers/connection_not_found-trigger.md)

### [get\_database\_name](../../built-in-functions/sodium-built-in-functions/database-related-functions/get_database_name.md)

### [get\_database\_type](../../built-in-functions/sodium-built-in-functions/database-related-functions/get_database_type.md)

### [Active Database Connection](../active-database-connection.md)

