# Applications Required

Development tools required to have  

* Development IDEs
  * Visual Studio 2019 Community Edition
  * Visual Studio Code
* Msys2
  * pacman -Syu
  * pacman -S base-devel gcc vim cmake
    * cmake --version

      cmake version 3.17.3

    * gcc --version

      gcc \(GCC\) 9.3.0

    * 
  * pacman -S tar
  * download and extract llvm-9.0.1 source
  * tar -xvf llvm-9.0.1.src.tar.xz
  * mkdir llvmbuild
  * cd llvmbuild
  * cmake -DCMAKE\_BUILD\_TYPE=Release ../llvm-9.0.1.src
  * cmake --build .
* Databases
  * Oracle
  * Ms Sql Server
  * Mysql
  * Postgresql
* 


