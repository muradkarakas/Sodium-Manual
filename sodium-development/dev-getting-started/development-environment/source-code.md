# Source Code

## Download All Sodium Project Repositories As Submodule

Follow the steps below in order to download Sodium source code

1. If you do not have `git` installed on your system. Download it from [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Open a new console window. \(Press `Start + R` and type the command below then click Ok.\)

   `cmd`

3. Move to root directory of `C:` drive

   `cd c:\`

4. Run the command below to download all Sodium projects at once. \(If you want to install Sodium into different folder name other than `c:\Sodium`, you need to change many project settings\)

   `git clone --recursive https://github.com/muradkarakas/Sodium.git`

{% hint style="info" %}
Sodium repository is a parent Visual Studio solution to ease download process. It has consist of `git submodules` to main Sodium project's repositories. So, Sodium repository does not provide you the latest nightly build version of Sodium projects. Just you get a special version of all Sodium projects. For detail on Git Submodule feature, have a look at that page [https://www.atlassian.com/git/tutorials/git-submodule](https://www.atlassian.com/git/tutorials/git-submodule)
{% endhint %}

## Download All Sodium Project Repositories Seperately

1. Open a new console window. \(Press `Start + R` and type the command below then click Ok.\)

   `cmd`

2. Move to root directory of `C:` drive
3. Create a folder named Sodium

   `mkdir c:\Sodium`

4. Change current directory

   `cd c:\Sodium`

5. Run all commands below step by step

```text
git clone https://github.com/muradkarakas/SodiumDebugger.git
git clone https://github.com/muradkarakas/SodiumServer.git
git clone https://github.com/muradkarakas/SodiumExtension.git
git clone https://github.com/muradkarakas/DBInt.git
git clone https://github.com/muradkarakas/DBInt-Postgresql.git
git clone https://github.com/muradkarakas/DBInt-Oracle.git
git clone https://github.com/muradkarakas/DBInt-SqlServer.git
git clone https://github.com/muradkarakas/DBInt-MySql.git
git clone https://github.com/muradkarakas/SodiumShared.git
git clone https://github.com/muradkarakas/DebuggerAdaptor.git
git clone https://github.com/muradkarakas/Sodium-Setup.git
```

