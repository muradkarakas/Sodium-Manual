
# What is HT/SQL ?
 
   HT/SQL is a new Software Language (actually it is a Domain-specific language) especially designed for creating/developing state of the art web based Business applications. It has been under development at the moment but ready to be evaluated by the developers.

# Who is developer ?

   Me.

# Development Technologies ?

  C Language with libraries listed below:
  --------
  - Parser  :
     The Lemon LALR(1) Parser Generator (https://www.sqlite.org/lemon.html)

  - Lexer   :
     Winflex (https://github.com/lexxmark/winflexbison)

  - Oracle Library:
     OCILIB (http://vrogier.github.io/ocilib/)

  - PostgreSQL Library: 
     Libpq - (https://www.postgresql.org/docs/9.1/libpq.html)

  - Redis Client Library:
     Hiredis (https://github.com/redis/hiredis)

# Why HT/SQL ? 

  * Specially Tailored for CRUD Application
  * Native SQL support
    You can write SQL command/scripts in code behind file as native language commands (Transact-SQL for MS SQL Server, PL/SQL for Oracle)
  * Server and Client Side support
    Current web based languages/frameworks are designed to run either on server or client. HT/SQL is designed to run on both. All things are handled HT/SQL engine transparently.
  *  No dependency
  * Easy to learn 
  * Native In-Memory database support
  * Easy to maintain
    All requirements are handled in a standard way so developers easily find the code blocks to make corrections.
  * Quick and Easy Installation: No database repository needed, No ODBC or OLE DB installation/configuration needed.
  * Basic HTML knowledge for visual design
  * Built-in AJAX and Mobile support
  * Fast
    
# How does it works ?

   HT/SQL is a Native ISAPI extension with 5 DLL (dynamic linked library) files. Whenever a *.frmx file request (with frmx extension) has been made to the IIS (Internet Information Server), IIS loads and delivers that request to the HT/SQL ISAPI extension.
