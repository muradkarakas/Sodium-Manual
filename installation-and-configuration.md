# Installation & Configuration

## Notes

Since PostgreSQL latest version does not support OID \(Object ID\), current version of Sodium does not support PostgreSql. However, previous versions of PostgreSql database are supported. Adding support to latest version is in my Todo list.

## Installation Steps

### 1. Download and Install "_Microsoft visual c++ 2015 redistributable package \(x64\)_"

Sodium is developed with C language. This package is needed to run C application.

{% embed url="https://www.youtube.com/watch?v=XET46fgTp5g" %}

{% embed url="https://www.microsoft.com/en-us/download/details.aspx?id=48145" %}

### 2. Download and Install "_Oracle Express Windows 64 Bit Edition_"

Sodium needs Oracle _**native client library**_ to access Oracle database instance.

{% embed url="https://www.youtube.com/watch?v=CrTo\_XoDQwI" %}

{% embed url="https://www.oracle.com/database/technologies/xe-downloads.html" %}

### 3. Download and Install "_PostgreSQL Database Windows 64 Bi_t"

Sodium needs PostgreSQL _**native client library**_ to access PostgreSQL database instance.

{% embed url="https://www.youtube.com/watch?v=e1MwsT5FJRQ" %}

{% embed url="https://www.enterprisedb.com/downloads/postgres-postgresql-downloads" %}

### 4. Download Sodium package

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
        <p><b>(See Note No.1)</b>
        </p>
      </td>
      <td style="text-align:left">
        <p>Oracle Database 18.4 Express Edition 64 Bit</p>
        <p>PostgreSQL-12.2.1</p>
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
1.  **For ORACLE:**  Check the path of the "oci.dll" file is exists in the system environment variable `PATH`. If not, please add.  Setting character encoding to UTF8 on the web server is required for Oracle. Otherwise, characters read from database cannot be seen as expected on the client browser. Please set character encoding part of the NLS\_LANG value to UTF8 on web server. \(Ex: TURKISH\_TURKEY.UTF8\).  **For POSTGRESQL:**  Check the path of the "libpq.dll" file is exists in the system environment variable `PATH`. If not, please add. For PostgreSQL database, Tables must be created "with OID" option. Otherwise, data blocks will be read only..
2. Do not use space character in installation path. Use only ANSI characters in installation path.
3. Add sodium installation path to the "Path" system environtment variable
{% endhint %}

