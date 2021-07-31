# openjdk11-src


## 说明

此仓库是openjdk11的源码，从openjdk官网下载，目的是以后看源码的时候添加注释记录下来。

## 编译openJdk11

首先下载openjdk11源码，进入[官网](http://jdk.java.net/java-se-ri/11)，在 **RI Source Code** 下面下载zip file即可。

解压后目录里面的src就是仓库的代码。

## 编译命令

```bash
bash configure --with-toolchain-type=clang --with-debug-level=slowdebug --enable-dtrace --with-jvm-variants=server --with-target-bits=64 --enable-ccache --with-num-cores=8 --with-memory-size=8000 --disable-warnings-as-errors --with-sysroot=/Library/Developer/CommandLineTools/SDKs/MacOSX10.14.sdk --with-boot-jdk=/Users/lionel/Environment/openjdk10/jdk-10.jdk/Contents/Home
```

```
make all
```

后期修改源码，添加注释后，使用`make image`进行增量编译即可。
