This directory stores the compiled versions of the Argon2 C library.

The subfolders must have the name of the platform, for which the library has been compiled. See [the JNA documentation](https://java-native-access.github.io/jna/4.5.0/javadoc/com/sun/jna/NativeLibrary.html) for details. You can use [this tool](https://github.com/phxql/jna-info) to retrieve the platform name.

The libraries are compiled from [this source code](https://github.com/P-H-C/phc-winner-argon2/releases/tag/20171227).

## Linux:
* x64: `make clean && CFLAGS=-m64 OPTTARGET=generic make`
* x86: `make clean && CFLAGS=-m32 OPTTARGET=generic make`
* arm: `make clean && make`
* arm-64: `make clean && make`

## Windows
Compiled with Visual Studio 2017, `ReleaseStatic` configuration

## OSX:
* `make clean && OPTTARGET=generic make`

# Cross compiling on Debian Linux

## arm
* `apt install gcc-arm-linux-gnueabihf`
* `make clean && CC=arm-linux-gnueabihf-gcc make`

## arm-64: 
* `apt install gcc-aarch64-linux-gnu`
* `make clean && CC=aarch64-linux-gnu-gcc make`
