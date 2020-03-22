# "user\_session\_end" trigger

#### Description

 `user_session_end` trigger has some special feature, Therefore, it must be use in care.

* `user_session_end` trigger function must be in [Controller File](../program-structure/controller-file.md).
* `user_session_end` trigger is executed in "no session" context. Therefore, built-in functions, variables etc are not valid in that trigger function.
* Only data available is the arguments.

**Declaration**

```text
void user_session_end(char reason, char client_ip_address, char client_domain, char client_os_user, char user_session_start_time);
```

#### **Parameters**

 **`reason`** ``: holds the information about why the session is ended.  
 **`client_ip_address`**: not implemented yet  
 **`client_domain`** ``: not implemented yet  
 **`client_os_user`** ``: not implemented yet  
 **`user_session_start_time`**: not implemented yet

#### **See also**

