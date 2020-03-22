# Datalist & Select Element Usage

This demo page shows:

* how to use [Data List](https://sodium.gitbook.io/sodium/language-reference/html-tags/sodium-tags/data-list) tag, [populate\_datalist](datalist-and-select-element-usage.md) function and record set variables
* how to fill a drop down list with a [Data List](https://sodium.gitbook.io/sodium/language-reference/html-tags/sodium-tags/data-list) tag
* how to define a look up select element

Create a new sub folder named `selectElement` under the `site\pages` folder of the installation path.

 **Form File:** 

Create a file named `selectElement.frmx` and copy/paste the code block showed below into the file.

```text
<!DOCTYPE html>
  
 <html>
  
    <head>
       <title>Select Element Demo</title>
    </head>
  
    <body>
    
       <datalist id="provinces"></datalist>
  
       <datalist id="counties"></datalist>
  
       <controlblock control-block-name="cb1">
          <select style="width: 100px" name="province_id"
             datalist-name="provinces">
          </select>
       </controlblock>
       
       <controlblock control-block-name="cb2">
          <select style="width: 100px" name="county_id" datalist-name="counties" 
             lookup-input-block-name="cb1" lookup-input-name="province_id">
          </select>     
       </controlblock>
       
    </body>
 </html>
```

 **Code behind File:** 

Create a file named `selectElement.sqlx` and copy/paste the code block showed below into the file.

```text
void page.load() {      
         
         rsProvinces =   select province_name as label, province_id as value
                                         from
                                                 provinces
                                         order by
                                           province_name;
         populate_datalist('provinces', rsProvinces);
  
         rsCounties =    select county_name as label, county_id as value, province_id as province_id
                                         from
                                                 counties
                                         order by
                                           county_name;
         populate_datalist('counties', rsCounties);
 }
```

 **Controller File:**

```text
void connection_not_found(char connectionName) {
         
         if (connectionName == 'default') then
                 bool connStatus;
                 connStatus = create_oracle_connection('default', 'XE', 'htdemo', '1234'); 
         end if;
         
 }
```

 **Output:**

![](https://gblobscdn.gitbook.com/assets%2F-M1F9jN2PZ8B8ILKwygX%2F-M24iU6bndfdhCFk9PIl%2F-M24jYCr712tA8stW0nY%2Fimage.png?alt=media&token=9ce641d6-da1b-4c95-be84-fa6afb849170)

