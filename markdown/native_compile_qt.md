# Native Compiled Qt Setup Guide

+ Download the prebuild release. Extract the file to `/opt`

```SHELL
sudo tar xvf qt-5.12.12-aarch64.tar.gz -C /opt
```

+ Setup enviroment

```SHELL
echo "export PATH=/opt/qt-5.12.12/bin:$PATH" >> ~/.bashrc
source ~/.bashrc
```

+ Try qmake.

```SHELL
qmake --version
```

# Intergrated with qtcreator

See [Intergrated_Guide](./cross_compile_qt.md#intergrated-with-qtcreator).


**Note:** In native compile, both your binaries and libraires are aarch64 object, so feel free to use the qtcreator for building or executing.