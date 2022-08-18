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

![default-exampleproject-Crc0UU40Zwoizw.png](http://flutter-media.knowledge.ituknown.cn/CreateFlutterProject/default-exampleproject-Crc0UU40Zwoizw.png)

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
-t                      指定创建的项目类型（app、module、package 或 plugin）, 默认 app
```

来看下具体示例：

```bash
$ flutter create --org "com.ituknown" --description "biu biu biu." -i objc -a java biu_project

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

![custom-exampleproject-0Biq1AZGKl8BaA.png](http://flutter-media.knowledge.ituknown.cn/CreateFlutterProject/custom-exampleproject-0Biq1AZGKl8BaA.png)

是不是很 nice~