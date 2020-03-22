# Code Behind File

* Code behind files are the files with \*.sqlx extension.
* Code behind files are used to separate application code with HTML.
* Each [Form File](https://muradkarakas.github.io/Sodium-Manual/frmx_file.html) has a code behind file with the same name but with ".sqlx" extension.
* Code behind files are automatically loaded and parsed just before the corresponding form file \(frmx file\) is parsed.
* Mostly used to hold page specific variables and functions' definitions. For functions and variables related to business logic, please use [Controller File](https://muradkarakas.github.io/Sodium-Manual/controller_file.html).

Developer can;

* write a special ["page.access" trigger](https://muradkarakas.github.io/Sodium-Manual/page_access.html) function in each code behind file in order to control page access.
* write a special ["page\_load" trigger](https://muradkarakas.github.io/Sodium-Manual/page_load.html) function to run code blocks funcafter form file parsing and before sending its content.

