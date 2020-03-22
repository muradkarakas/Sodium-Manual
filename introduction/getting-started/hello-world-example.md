# Hello World Example

Create a new sub folder named `helloworld` under the `Sodium-Site\apps` folder of the installation path.

 **Form File:** Create a file named `helloWorld.frmx` and copy/paste the code block showed below into the file.

```text
<!DOCTYPE html>
  
 <html>
         <head>
                 <title>Hello World</title>
         </head>
  
         <body>
  
                 <controlblock control-block-name="cbDemo">
                         <input name="say" type="button" value="Say Hello World" />
                 </controlblock>
  
         </body>
 </html>
```

 **Form File Explanation:**

* It is a plain html file. The only difference is a `controlblock` tag on line 10 and 12 with a name `control-block-name="cbDemo"`. For more information on control blocks, please follow the link [Control Block](https://sodium.gitbook.io/sodium/language-reference/html-tags/sodium-tags/control-block).
* There is nothing special about the input tag in the control block. For more information on buttons, please follow the link [Button Item](https://sodium.gitbook.io/sodium/language-reference/html-tags/html-tags/inputs/button-item).

 **Code behind File:** Create a file named `helloWorld.sqlx` and copy/paste the code block showed below into the file.

```text
void page.load() {
         message('Page loaded');
 }
  
 void cbDemo.say() {
         message('Hello World');
 }
```

**Code behind Explanation:**

* Each form file must have a code behind file in the same directory. Code behind files has the same name but with `sqlx` extension. For more information on Code Behind files, please follow the link [Code Behind File](https://sodium.gitbook.io/sodium/language-reference/program-structure/code-behind-file).
* In the ["page\_load" trigger](https://sodium.gitbook.io/sodium/language-reference/built-in-triggers/page-level-triggers/page_load-trigger), [message](hello-world-example.md) function is used in order to show a message on the client browser.

**Output:** In order to open page, write the form file path into the address bar of the Internet browser. After each file request, "Page loaded" will be shown. For each click on "Say Hello World" button, "Hello World" message will be shown.

![](https://gblobscdn.gitbook.com/assets%2F-M1F9jN2PZ8B8ILKwygX%2F-M24jeGZ97JH351E3RO6%2F-M24jmRwdvGVdvGRZeHF%2Fimage.png?alt=media&token=5aa43186-fdd0-49c4-b520-0a560f5d30c3)

