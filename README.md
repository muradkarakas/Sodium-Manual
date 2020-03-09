
# What is Sodium ?
 
   Sodium is a new Software Language (actually it is a Domain-specific language) especially designed for creating/developing state of the art web based Business applications. It has been under development at the moment but ready to be evaluated by the developers.

# Who is developer ?

   Me.

# Development Technologies ?

  C Language and Other libraries listed below:
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

# Why Sodium ? 

  * Specially Tailored for CRUD Application
  * Native SQL support: 
    You can write SQL command/scripts in code behind file as native language commands (Transact-SQL for MS SQL Server, PL/SQL for Oracle)
  * Server and Client Side support: 
    Current web based languages/frameworks are designed to run either on server or client. Sodium is designed to run on both. All things are handled Sodium engine transparently.
  *  No dependency
  * Easy to learn 
  * Native In-Memory database support
  * Easy to maintain: All requirements are handled in a standard way so developers easily find the code blocks to make corrections.
  * Quick and Easy Installation: No database repository needed, No ODBC or OLE DB installation/configuration needed.
  * Basic HTML knowledge for visual design
  * Built-in AJAX and Mobile support
  * Fast
  
# Components:
  
  Sodium is a Native Windows Application having these components;
  * SodiumServer.exe:
    Generic Native Http Server
    
  * SodiumDebugger.exe:
    Native GNU Debugger (GDB)
    
  * DBInt.dll, DBInt-Oracle.dll and DBInt-Postgresql.dll:
    Sodium-To-Database interface & implementation files
  
  * SodiumExtension.dll:
    Sodium language Http Server plug-in
    
# How does it works ?:

  Whenever a *.frmx file request (with frmx extension) has been made to the Generic Native Http Server (SodiumServer.exe), It delivers that request to the Sodium Server plug-in (SodiumExtension.dll). Sodium plug-in process the request and response accordingly. 
  
# Roadmap: 

  * Planning to run Sodium as a standalone web server. That is there will be no dependency to IIS. 
  * Adding Https support
  * Adding Server Sent Events (SSEs) support

# Documentation:

 https://muradkarakas.github.io/Sodium-Manual/
