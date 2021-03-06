---
description: Be sure to not miss out on new features and improvements!
---

# Change Log

## 2020-05-30 \(Version 0.0.8\)

### Bug fixes

* A serious bug detected in `DBInt-PostgreSql.dll` file. Memory locations holding sql command parameter values were overwritten by random values. \(Postgresql library requires a dynamically sized pointer array to another pointer which holds actual paramater values of SQL statement. \(More detail: `paramValues` parameter of the [PQexecParams](https://www.postgresql.org/docs/current/libpq-exec.html) function\)

### **Improvements**

* [Troubleshooting ](../installation-and-configuration.md#troubleshooting)section is added to the [Installation & Configuration page](../installation-and-configuration.md). 
* MS Sql Server support is added.

## 2020-05-12 \(Version 0.0.7\)

### Bug fixes

* In case[`page.access`](../language-reference/built-in-triggers/page.access-trigger.md) trigger returns `false`, http response was not generated correctly. 
* Some C functions related to blob column type operations for MySql database are modified/fixed.
* Some memory areas allocated for Page Object and its properties was not released properly.
* [MySql demo database creation script file](https://github.com/muradkarakas/Sodium-Setup/blob/master/Sodium-Site/mysql_demo_installation.sql) fixed.

## 2020-05-10 \(Version 0.0.6\) <a id="2020-05-01-version-0-0-5"></a>

### Improvements

* Mysql Support added \([create\_mysql\_connection](../language-reference/built-in-functions/sodium-built-in-functions/database-related-functions/create_mysql_connection.md)\)

### Bug fixes

* C functions related to reading/writing blob data to/from database is not working with Http Server API. Migration from Microstf Internet Information Server to Http Server API is not complete.

## 2020-05-01 \(Version 0.0.5\)

### Improvements

* Table/view primary key column name is automatically populated from database schema dictionary if not provided by developer.
* For the data blocks whose [auto-generated-columns](../language-reference/tags/data-block/#auto-generated-columns-property) property is set to TRUE, table/view primary key column name is automatically populated from database schema dictionary.

## 2020-04-30 \(Version 0.0.4\)

### Bug fixes

* Page expire time calculation was wrong. It is fixed.
* Postgresql Demo was not working due to database row identifying strategy. It is replaced with new one \(see Improvements for deail\).

### Improvements

* Demo database objects are created in SODIUM\_DEMO user in Oracle Container database \(with using "alter session set "\_ORACLE\_SCRIPT"=true;" command\). After this modification, demo database user names for both Oracle and Postgresql are same. 
* Pseudo columns 

  * `oid` in Postgresql database
  * `rowid` in Oracle database

  are not used anymore. Developer must set [key-column-name](../language-reference/tags/data-block/#key-column-name-property) property if he/she want to have a writable datablock.

## 2020-04-29 \(Version 0.0.3\)

### Improvements

\`\`[`key-column-name`](../language-reference/tags/data-block/#key-column-name-property)property added to the [data block tag](../language-reference/tags/data-block/).

## 2020-04-28 \(Version 0.0.2\)

### Bug fixes

While parsing string literals in sqlx files, &lt; and &gt; characters are not copied into string. Sqlx file lexer fixed.

## 2020-04-23 \(Version 0.0.1\)

### Improvements

From now on, pNotify is used as client library for [`message` ](../language-reference/built-in-functions/sodium-built-in-functions/other-functions/message.md)function. And also, a new variant has been added to message function.

