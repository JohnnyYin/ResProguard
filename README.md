# ResProguard
Android resources Proguard.  
参考美团的思路：[http://tech.meituan.com/mt-android-resource-obfuscation.html](http://tech.meituan.com/mt-android-resource-obfuscation.html)

# 编译
基于 Android6.0.0_r1 进行编译.
* 首先需要下载好Android源码，可以参考:[http://source.android.com/source/initializing.html](http://source.android.com/source/initializing.html)
* 然后clone下ResProguard源码
* 替换aapt源码，aapt源码目录为 frameworks/base/tools/aapt，主要替换[Resouce.cpp](https://github.com/JohnnyYin/ResProguard/blob/master/Resource.cpp)文件；
* 然后在源码根目录执行
```
source build/envsetup.sh;
mmm frameworks/base/tools/aapt;
```
编译好的输出目录为：
```
out/host/darwin-x86/bin/aapt # darwin-x86 根据系统环境不同而不同
```

由于编译过程比较复杂，release中提供了mac osx编译好的版本：[aapt 23.0.1 for mac osx](https://github.com/JohnnyYin/ResProguard/releases/download/v1.0/aapt)

# License
The MIT License (MIT)
