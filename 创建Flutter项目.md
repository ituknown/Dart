# 创建默认项目

创建 Flutter 项目只需要一个简单的命令即可：

```bash
$ flutter create project-name
```

`project-name` 是你的具体项目名，也可以是一个文件路径。示例：

```bash
$ flutter create path/exampleproject

Creating project path/exampleproject...
Running "flutter pub get" in exampleproject...                          1,331ms
Wrote 127 files.

All done!
In order to run your application, type:

  $ cd path/exampleproject
  $ flutter run

Your application code is in path/exampleproject/lib/main.dart.
```

这样，一个 Flutter 项目就创建完成了：

![default-exampleproject-Crc0UU40Zwoizw.png](https://ituknown.org/dart-media/CreateFlutterProject/default-exampleproject-Crc0UU40Zwoizw.png)

要注意的一点是，项目名（`exampleproject`）必须是 `[a-z0-9_]` 组合，不能包含 `-` 等字符。

# 创建项目时指定基础信息

[创建默认项目](#创建默认项目) 虽然简单，但是很多默认的项目信息显然不是我们想要的，比如项目的默认组织信息是 `com.example`。

因此，在创建项目是我们最好加上一些可选参数，做下基本的信息配置。命令如下：

```bash
$ flutter create [options] project-name
```

 `options` 就是我们在创建项目时要使用的可选参数了，最常用的有如下四个可选参数：

```bash
--org                   指定项目组织, 默认 "com.example"
--description           指定项目描述信息, 默认 "A new Flutter project."
-i, --ios-language      指定 IOS 开发语言（objc 或 Swift）, 默认 Swift
-a, --android-language  指定 Android 开发语言（java 或 kotlin）, 默认 kotlin
-t, --template          指定创建的项目类型（app、module、package 或 plugin）, 默认 app

--platforms             指定创建的应用平台（ios/android/windows/linux/macos/web）,默认会创建全部平台
```

比如下面这个创建项目的命令示例：

```bash
$ flutter create --org com.ituknown --template=app --description "biu biu biu." -i objc -a java biu_project
```

其中 `com.ituknown` 是项目包名的一部分，`biu_project` 是具体项目名称。该项目的完整包名为：`com.ituknown.biu_project`。

下面是命令输出示例：

```bash
Creating project biu_project...
Running "flutter pub get" in biu_project...                      1,323ms
Wrote 128 files.

All done!
In order to run your application, type:

  $ cd biu_project
  $ flutter run

Your application code is in biu_project/lib/main.dart.
```

现在再来看下项目信息：

![custom-exampleproject-0Biq1AZGKl8BaA.png](https://ituknown.org/dart-media/CreateFlutterProject/custom-exampleproject-0Biq1AZGKl8BaA.png)

如果想要创建指定平台的应用，只需要使用 `--platforms` 参数指定即可，比如只创建桌面应用（windows/macos/linux）：

```bash
$ flutter create --org com.ituknown --platforms windows,macos,linux example_project
```

是不是很 nice~