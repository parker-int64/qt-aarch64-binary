# qt-aarch64

由于部分国产主机采用的是armv8架构CPU，在编译部分qt程序时会遇见版本较低的情况。软件包管理中也无法安装更新版本。于是专门编译aarch64架构下的qt，可直接下载后设置环境变量使用。

## 通用方式

目前编译好的文件分为两种形式：

1. 交叉编译版本：此版能在x86_64上的Linux系统进行编译，前提需要一个交叉编译器，此处采用的是[gcc-Linaro](http://releases.linaro.org/components/toolchain/binaries/),只需下载合适版本的编译器，便可以交叉编译aarch64可执行文件。将可执行文件和库文件复制到aarch64主机上便可以运行。


目前对应的情况如下：

|Ubuntu 版本|主机GCC版本|交叉编译器GCC版本|
|----|----|----|
|16.04|gcc-5|gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu|
|18.04|gcc-7|gcc-linaro-7.5.0-2019.12-x86_64_aarch64-linux-gnu|

更多等待添加...


2. 本地编译版本：直接在aarch64架构主机上编译的qt，此版本设置好环境变量后直接可以使用，使用原生编译器即可。

所有的编译尽量降低了平台无关性，也可以尝试使用更高版本编译器进行编译，（让我知道哪些能用更好）。


3. 与qtcreator结合使用： 需要在qtcreator的kits中设置qmake和编译器。可以参考[看图就知道设置什么](./cross_compile_qt.md#intergrated-with-qtcreator)

有能力还是别用qtcreator... 自己动手写（QtWidgets, qml）吧。我都不知道放个库上来会不会违反LGPL协议。