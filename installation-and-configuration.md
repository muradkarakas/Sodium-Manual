# Installation & Configuration

## Installation Notes

---

## Installation Steps

### 1. Download and Install "_Microsoft Visual C++ 2015 Redistributable Package \(x64\)_" if not already installed. If you have already, skip this step.

Sodium is developed with C language. This package is needed to run C application.

{% embed url="https://www.youtube.com/watch?v=XET46fgTp5g" %}

{% embed url="https://www.microsoft.com/en-us/download/details.aspx?id=48145" %}

### 2.  Download Sodium package

Download package is nightly built versions of Sodium. Do not try it on live/production database and web servers.

Please report errors/problems you encounter to the following contact points:

Developer E-Mail: [muradkarakas@gmail.com](https://muradkarakas.github.io/Sodium-Manual/download_page.html#) 

LinkedIn Profile Page: [http://tr.linkedin.com/in/muradkarakas](http://tr.linkedin.com/in/muradkarakas)

{% embed url="https://github.com/muradkarakas/Sodium-Setup" %}

Youtube playlist for installation \(2 videos\)

{% embed url="https://www.youtube.com/playlist?list=PLMDu6aYdBVG3LmDAnX1FDYFyS9F3qkeEV" %}

## Prerequisites & Troubleshooting

<table>
  <thead>
    <tr>
      <th style="text-align:left"><b>Category</b>
      </th>
      <th style="text-align:left"> <b>Software</b>
      </th>
      <th style="text-align:left"> <b>Tested on</b>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Operation System</td>
      <td style="text-align:left">MS Windows 64 Bit</td>
      <td style="text-align:left">
        <p>Windows Server 2012 64Bit</p>
        <p>Windows 10 64Bit</p>
        <p>Windows 7 Professional 64Bit</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Database Server</td>
      <td style="text-align:left">
        <p>Oracle</p>
        <p>PostgreSQL</p>
        <p>MySql</p>
        <p><b>(See Note No.1)</b>
        </p>
      </td>
      <td style="text-align:left">
        <p>Oracle Database 18.4 Express Edition 64 Bit</p>
        <p>PostgreSQL-12.2.1</p>
        <p>MySql</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Internet Browser</td>
      <td style="text-align:left">
        <p>Mozilla Firefox</p>
        <p>Google Chrome</p>
        <p>Microsoft Internet Explorer Opera</p>
      </td>
      <td style="text-align:left">Latest Versions</td>
    </tr>
    <tr>
      <td style="text-align:left">System Resource (Port)</td>
      <td style="text-align:left">&#x200B;</td>
      <td style="text-align:left">
        <p>Installation script installs Sodium on port 8089 by default.</p>
        <p>If this port is used by another application, please find and open StartSodiumServer.bat
          file, modify port parameter and save it.</p>
      </td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
1. **For ORACLE:**  
   Check the path of the "oci.dll" file is exists in the system environment variable `PATH`. If not, please add.  
   Setting character encoding to UTF8 on the web server is required for Oracle. Otherwise, characters read from database cannot be seen as expected on the client browser. Please set character encoding part of the NLS\_LANG value to UTF8 on web server. \(Ex: TURKISH\_TURKEY.UTF8\).  
   **For POSTGRESQL:**  
   Check the path of the "libpq.dll" file is exists in the system environment variable `PATH`. If not, please add. 

   **For MySql:**

   Check the path of the "libmysql.dll" file is exists in the system environment variable `PATH`. If not, please add.

2. Do not use space character in installation path. Use only ANSI characters in installation path.
{% endhint %}



