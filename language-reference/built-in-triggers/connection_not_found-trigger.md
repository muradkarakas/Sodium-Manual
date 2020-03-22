# "connection\_not\_found" trigger

#### Description

 Whenever a connection is needed and it does not exist, `connection_not_found` trigger is fired.  
 Sodium developer must create a new named connection with the same name as specified in `connectionName` parameter in the trigger function by calling one of these functions : [create\_oracle\_connection](../built-in-functions/sodium-built-in-functions/database-related-functions/create_oracle_connection.md) or [create\_postgresql\_connection](../built-in-functions/sodium-built-in-functions/database-related-functions/create_postgresql_connection.md).

**Declaration**

```text
void connection_not_found(char connectionName);
```

#### **Example**

#### \*\*\*\*

#### **See also**

 [Database Connections](../connection/connection-types/database-connections.md)  
 

