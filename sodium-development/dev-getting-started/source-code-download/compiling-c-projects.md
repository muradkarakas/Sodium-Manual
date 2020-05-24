# Compiling C Projects

## How to Compile C Projects

* In order to compile all C projects, you must download and install a few more applications listed below.
  * Oracle Database Express Edition \(XE\) 64Bit
  * PostgreSQL Datavase 64Bit
  * MySql Database Server 64Bit
  * MS Sql Server 64Bit
  * Redis Server 64Bit
* Add `C:\Sodium\Sodium-Setup` path to the system `PATH` environment variable.
* Add database libray paths to the system `PATH` environment variable.
* Run Visual Studio 2019 Community Edition as administrator. Then find and open `c:\Sodium\Sodium.sln` solution file.
* Compile and link in `Debug` or `Release` profile with 64Bit CPU architecture.
* If you get `library/dll file not found` error message during linkage, please modify project settings according to database library paths.

