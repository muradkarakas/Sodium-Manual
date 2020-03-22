# Active Database Connection

## Description

*  **Active Database Connection** term is used to determine which database connection will be used if database connection name is not specified by developer in application source code.
*  Initially, **Active Database Connection** is NULL. After the first successful attempt to open a new database connection has been made, **Active Database Connection** points to that connection.
*  In some specific user functions, **Active Database Connection** is automatically redirected to the any one of the specific database connection.
  *  For the trigger functions of a &lt;datablock&gt; element or an &lt;input&gt; element in a data block, **Active Database Connection** is automatically points to data block's connection.
*  **Active Database Connection** can be set by using [set\_active\_database\_connection](../built-in-functions/sodium-built-in-functions/database-related-functions/set_active_database_connection.md) in any user function. Sodium engine backups current active connection before execution of a user function begins. After execution of a user function ends, Sodium engines restores the original active connection setting back. Therefore, effects of [set\_active\_database\_connection](../built-in-functions/sodium-built-in-functions/database-related-functions/set_active_database_connection.md) call is valid only in the function which is currently being executed.

## See also

###  [set\_active\_database\_connection](../built-in-functions/sodium-built-in-functions/database-related-functions/set_active_database_connection.md)

