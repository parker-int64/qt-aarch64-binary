# Setup your cross compiler
Get a cross compiler from [GCC-Linaro](http://releases.linaro.org/components/toolchain/binaries/)


(Don't ask me why I'm not using the package manager provided cross compiler. It simply doesn't work well.)

+ **Q**: Select a version ?

Get the cross compiler that is suitable for your host and target system.

Currently, my cross compiler's version is based on the ubuntu default compiler's version:

|Ubuntu Version|Host GCC Version|Target Cross Compiler Version|
|----|----|----|
|16.04|gcc-5|gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu|
|18.04|gcc-7|gcc-linaro-7.5.0-2019.12-x86_64_aarch64-linux-gnu|

More to be add...


Not sure if the higher version would work. You are welcom to try it and let me know! &#x1F603;

## Decompress and setup PATH

eg:

```SHELL
sudo tar xvf gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu.tar.xz -C /opt

echo "PATH=/opt/gcc-linaro-5.5.0-2017.10-x86_64_aarch64-linux-gnu/bin:$PATH" >> ~/.bashrc

source ~/.bashrc
```

## Try the compiler

```SHELL
$ aarch64-linux-gnu-gcc -v
Using built-in specs.
COLLECT_GCC=aarch64-linux-gnu-gcc
COLLECT_LTO_WRAPPER=/opt/gcc-linaro-gnu-aarch64/bin/../libexec/gcc/aarch64-linux-gnu/5.5.0/lto-wrapper
Target: aarch64-linux-gnu
Configured with: '/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/snapshots/gcc.git~linaro-5.5-2017.10/configure' SHELL=/bin/bash --with-mpc=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/builds/destdir/x86_64-unknown-linux-gnu --with-mpfr=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/builds/destdir/x86_64-unknown-linux-gnu --with-gmp=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/builds/destdir/x86_64-unknown-linux-gnu --with-gnu-as --with-gnu-ld --disable-libmudflap --enable-lto --enable-shared --without-included-gettext --enable-nls --disable-sjlj-exceptions --enable-gnu-unique-object --enable-linker-build-id --disable-libstdcxx-pch --enable-c99 --enable-clocale=gnu --enable-libstdcxx-debug --enable-long-long --with-cloog=no --with-ppl=no --with-isl=no --disable-multilib --enable-fix-cortex-a53-835769 --enable-fix-cortex-a53-843419 --with-arch=armv8-a --enable-threads=posix --enable-multiarch --enable-libstdcxx-time=yes --with-build-sysroot=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/sysroots/aarch64-linux-gnu --with-sysroot=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/builds/destdir/x86_64-unknown-linux-gnu/aarch64-linux-gnu/libc --enable-checking=release --disable-bootstrap --enable-languages=c,c++,fortran,lto --build=x86_64-unknown-linux-gnu --host=x86_64-unknown-linux-gnu --target=aarch64-linux-gnu --prefix=/home/tcwg-buildslave/workspace/tcwg-make-release/builder_arch/amd64/label/tcwg-x86_64-build/target/aarch64-linux-gnu/_build/builds/destdir/x86_64-unknown-linux-gnu
Thread model: posix
gcc version 5.5.0 (Linaro GCC 5.5-2017.10) 

```

And it's done!