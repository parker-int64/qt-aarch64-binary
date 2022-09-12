# qt-aarch64-binary

This repo holds precompiled qt sources for aarch64-linux (armv8), mostly used by Embeded Linux Devices.

# General Usage

There are currently two sorts of releases, the cross compiled and native compiled. 
+ The previous was compiled and mainly used in **x86_64**. When you setup the enviroment and the corss compiler correctly, you may build the binary file for target system. If you want to run it, send it to the target system and execute it.
+ The later one was used in native **aarch64** enviroment, just setup the enviroment, then you can build and run your applications natively.

## Cross Compile:

Before you setup the qt, you'll need to get a cross compiler. See [set_cross_compiler](./markdown/set_cross_compiler.md) for more details.

Follow the [cross_compile_qt](./markdown/native_compile_qt.md) for more instructions.



## Native Comile:

See [native_compile_qt](./markdown/native_compile_qt.md). for more details.