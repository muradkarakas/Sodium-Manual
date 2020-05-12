# Known Issues

## Restrictions:

* Only one blob / lob column can be inserted or updated by a single SQL command execution against **MySQL database**. Solution; until it is fixed, execute a specific insert/update command for each one of the BLOB columns successively. If you try to update/insert more than one blob column in a single SQL command, first column data will be stored in all blob columns repeatedly.

