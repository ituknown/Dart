安装 `hover`：

```bash
$ go install github.com/go-flutter-desktop/hover@latest

$ hover version
Hover v0.47.1
```

|**注意**|
|:------|
|`go install` 命令会将程序安装到 `$GOPATH/bin` 目录下。因此，如果你没有配置环境变量：（`export PATH=$PATH:$GOPATH/bin`）的话，是没法直接使用 `hover` 命令的。|

创建 Flutter 项目：

```bash
$ flutter create exampleproject

Creating project exampleproject...
Running "flutter pub get" in exampleproject...                   1,538ms
Wrote 127 files.

All done!
In order to run your application, type:

  $ cd exampleproject
  $ flutter run

Your application code is in exampleproject/lib/main.dart.
```

进入项目根目录：

```bash
$ cd exampleproject
```

使用 `hover` 初始化 Go-Flutter 项目：

```bash
$ hover init

go: creating new go.mod: module exampleproject/go
go: to add module requirements and sums:
	go mod tidy
hover: You can add the '/Users/mingrn97/Desktop/tmp/exampleproject/go' directory to git.
go: finding module for package github.com/pkg/errors
go: finding module for package github.com/go-flutter-desktop/go-flutter
go: found github.com/go-flutter-desktop/go-flutter in github.com/go-flutter-desktop/go-flutter v0.52.2
go: found github.com/pkg/errors in github.com/pkg/errors v0.9.1
hover: Available plugin for this project:
```

运行 Go-Flutter 项目：

```bash
$ hover run
```

当我们第一次运行项目时（`hover run`）会提示找不到 `lib/main_desktop.dart` 文件，该文件是 `go-flutter` 的默认启动入口文件。

同时会给出提示询问是否创建该文件（记得选择 y），之后会自动创建该文件并启动程序。

下面是输出示例：

```bash
$ hover run

hover: Using engine from cache
hover: Cleaning the build directory
hover: Target file "lib/main_desktop.dart" not found.
hover: Let hover add the "lib/main_desktop.dart" file?
hover: [y/N]? y  # <== 选择 y
hover: Target file "lib/main_desktop.dart" has been created.
hover:        Depending on your project, you might want to tweak it.
hover: ⚠ The go-flutter project tries to stay compatible with the beta channel of Flutter.
hover: ⚠     It's advised to use the beta channel: `flutter channel beta`
hover: Bundling flutter app

💪 Building with sound null safety 💪

hover: Checking available release on Github
hover: 'hover' has an update available. (v0.47.1 -> 0.47.2)
hover:               To update 'hover' go to `https://github.com/go-flutter-desktop/hover#install` and follow the install steps
hover: Compiling 'go-flutter' and plugins
runtime/cgo
github.com/go-flutter-desktop/go-flutter/embedder
github.com/go-flutter-desktop/go-flutter/internal/currentthread
github.com/go-gl/gl/v3.3-core/gl
github.com/go-gl/glfw/v3.3/glfw
github.com/go-flutter-desktop/go-flutter/internal/priorityqueue
github.com/go-flutter-desktop/go-flutter/internal/opengl
github.com/go-flutter-desktop/go-flutter/internal/keyboard
github.com/go-flutter-desktop/go-flutter
exampleproject/go/cmd
hover: Successfully compiled executable binary for darwin
hover: Build finished, starting app...
hover: Running exampleproject in debug_unopt mode
flutter: The Dart VM service is listening on http://127.0.0.1:50300/
hover: Connecting hover to 'exampleproject' for hot reload
Syncing files to device Flutter test device...                      8.6s

Flutter run key commands.
r Hot reload. 🔥🔥🔥
R Hot restart.
h List all available interactive commands.
d Detach (terminate "flutter run" but leave application running).
c Clear the screen
q Quit (terminate the application on the device).

💪 Running with sound null safety 💪

An Observatory debugger and profiler on Flutter test device is available at: http://127.0.0.1:54624/dwMuq98OjIE=/
The Flutter DevTools debugger and profiler on Flutter test device is available at: http://127.0.0.1:9100?uri=http://127.0.0.1:54624/dwMuq98OjIE=/
```

--

https://hover.build

https://github.com/go-flutter-desktop/hover