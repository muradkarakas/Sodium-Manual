# Known Issues

## Restrictions

* Only one blob / lob column can be inserted or updated by a single SQL command execution against **MySQL database**. Solution; until it is fixed, execute a specific insert/update command for each one of the BLOB columns successively. If you try to update/insert more than one blob column in a single SQL command, first column data will be stored in all blob columns repeatedly.

## Need To Know

* Sodium uses [GetTickCount](https://docs.microsoft.com/en-us/windows/win32/api/sysinfoapi/nf-sysinfoapi-gettickcount) Windows API function to generate unique value for MySql database connections. See also;
  * [sequence-schema-name and seqeunce-name](../language-reference/tags/inputs/text-item.md#sequence-name-property) properties of [Text Item](../language-reference/tags/inputs/text-item.md).
  * [Sequences in Oracle](https://docs.oracle.com/cd/B28359_01/server.111/b28310/views002.htm#ADMIN11792)
  * [Sequences in PostgreSql](https://www.postgresql.org/docs/current/sql-createsequence.html)
  * MySql does not have Sequence object type

