# "page.access" trigger

#### Description

`page.access` trigger function is optional. if it is needed, must be in [Code Behind File](../program-structure/code-behind-file.md).

Whenever a [Form File](../program-structure/form-file.md) is requested, `page.access` function is called before procession file request.  
 If the function does **not exist**, this means that requested file is public and all requests are granted.  
 If `page.access` trigger function **exists** and;

* returns `true`, end users have been granted to access the page.
* returns `false`, the request has been refused.

**Since it runs before page processing starts, `page.access` trigger function has the following restrictions:**

* HTML elements defined in [Form File](../program-structure/form-file.md) \(like data/control blocks, data lists\) are not available/accessible in the trigger function code.
* Functions defined in [Code Behind File](../program-structure/code-behind-file.md) are not available/accessible also.

**What can be done in `page.access` trigger function:**

* For authentication: Executing SQL statement in order to get user credentials from database tables.
* For authorization: Executing SQL statement in order to get user privileges.
* Logging: Executing SQL statement in order to insert/update log tables.
* Setting/getting session variables.
* Reading/writing files on disk.

**Be careful:** Usage of the `page.access` trigger function in "log on pages" must not block to accessing that page. In other words, the trigger function for log on page must always return true if exists. Otherwise nobody authenticate themselves to the application.

**Declaration**

```text
bool page.access();
```

#### **Example**

```text
bool page.access() {
    return :Session.authenticated;
}
```

#### **See also**

