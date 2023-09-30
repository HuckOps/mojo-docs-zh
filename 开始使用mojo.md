mojo现在已经支持本地开发。

mojo当前可以在ubuntu系统开发，并且未来会支持macos和windows。到那时候我们的安装说明将包括如何在windows和macos上使用容器或者远程linux上开发。或者你可以在我们的页面[Mojo Playground](https://docs.modular.com/mojo/manual/get-started/#develop-in-the-mojo-playground)做实验。


## 安装mojo sdk

mojo sdk包含了在本地开发所用的一切，包括mojo标准库和[mojo命令行](https://docs.modular.com/mojo/cli/)（CLI）。Mojo cli可以在REPL程序环境启动、编译和运行源码文件，格式化源码文件等等。

我们也发布了[mojo vscode插件](https://marketplace.visualstudio.com/items?itemName=modular-mojotools.vscode-mojo)为Mojo api提供一流的开发体验，脑阔代码编写、快速修复和悬停帮助。

## 系统依赖

使用mojo sdk，你需要符合以下系统要求：

* Ubuntu 20.04/22.04 LTS
* x86-64 CPU (with SSE4.2 or newer) and a minimum of 8 GiB memory
* Python 3.8 - 3.10
* g++ or clang++ C++ compiler

将在未来的版本中支持macos和windows。

## 安装mojo

Mojo sdk可以通过[Modular CLI tool](https://docs.modular.com/cli/)像管理应用宝一样安装和更新mojo。用以下链接登录到Modular开发控制台，在这里可以获取Modular CLI和安装Mojo:

[获取Mogo sdk](https://developer.modular.com/download)

下来获取[Hello world](https://docs.modular.com/mojo/manual/get-started/hello-world.html)

## 更新mojo

Mojo正在发展，我们将发布mojo语言和SDK的更新。关于每个版本的信息可以可以看[Changelog](https://docs.modular.com/mojo/changelog.html)。

检查你正在使用的Mojo版本，使用```--version```选项：
```shell
mojo --version
```
更新到mojo最新版本，使用```modular update```命令：
```
modular update mojo
```


