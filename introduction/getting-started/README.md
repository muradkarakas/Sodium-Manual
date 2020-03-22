# Getting Started

## **What you should already know**

* SQL and vendor specific database scripting language \(PL/SQL for Oracle etc\)
* HTML \(Basic\)

## File Types

### **Form files:**

* Form files must have `frmx` extension
* Form files are actually HTML files with additional [TAGs](https://sodium.gitbook.io/sodium/language-reference/html-tags) and attributes. TAGS and attributes having special meaning in Sodium are listed in TAGs page.
* Form files must be well-formed and conform to HTML 5 standard. Otherwise, application will not work as expected
* While editing, using an HTML editor is strongly advised \(Eclipse, NetBeans, MS Visual Studio HTML editor, etc.\)
* These files must be UTF8 encoded

### **Code behind files \(sqlx files\)**

* SQLX files must have `sqlx` extension
* These files are used to separate code with HTML
* SQLX files are code behind files and consist of functions and global variables
* Although Sodium language is very similar to C or JavaScript language, it is actually completely new language and has its own grammar rules. So please have a look at the related pages in this manual
* These files must be UTF8 encoded

### **Controller files \(controller.sqlx\):**

* It is just an `sqlx` file with a special file name `controller.sqlx`
* The difference between regular code behind and Controller file is that the later is loaded once for the first request. For more information, [Controller File](https://sodium.gitbook.io/sodium/language-reference/program-structure/controller-file)​

## Some additional notes on file types

* For the current release of Sodium, all files must be in the same folder.
* All Form files must have a code behind file \(with the same name but `sqlx` extension\). For example, if you have `inventory.frmx` file, you must have `inventory.sqlx` file in the same folder even if it is empty.
* Sodium application can consist of more than one form file in order to implement the business logic but can only have one controller file.
* Form file paths are relative to path of the `SodiumServer.exe` file. So, for the current release, it is advised to create a new sub folder for your application under the `SodiumServer.exe` file location.
* Sodium projects must have controller file even if it is empty. Controller file must be in the same directory of the other forms/code behind files.

