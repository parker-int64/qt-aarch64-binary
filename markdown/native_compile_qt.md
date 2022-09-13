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

1. Setup kits, select Qt Version
![qt_version](../img/manage_kits_native_1.png)

2. Select compiler.

![qt_compiler](../img/manage_kits_native_2.png)

3. Apply settings in kits

![apply](../img/manage_kits_native_3.png)

With the right `qmake` and compiler, you may now build and run your app locally.