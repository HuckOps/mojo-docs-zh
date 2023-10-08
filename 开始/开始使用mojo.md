mojo现在已经支持本地开发。

mojo当前可以在ubuntu系统开发，并且未来会支持macos和windows。到那时候我们的安装说明将包括如何在windows和macos上使用容器或者远程linux上开发。或者你可以在我们的页面[Mojo Playground](https://docs.modular.com/mojo/manual/get-started/#develop-in-the-mojo-playground)做实验。


## 安装mojo sdk

mojo sdk包含了在本地开发所用的一切，包括mojo标准库和[mojo命令行](https://docs.modular.com/mojo/cli/)（CLI）。Mojo cli可以在REPL程序环境启动、编译和运行源码文件，格式化源码文件等等。

我们也发布了[mojo vscode插件](https://marketplace.visualstudio.com/items?itemName=modular-mojotools.vscode-mojo)为Mojo api提供一流的开发体验，包括代码编写、快速修复和悬停帮助。

![](https://docs.modular.com/static/images/mojo/mojo-vscode.png)

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

我们同样需要更新```modular```工具，如果用debian包管理器安装（目前只支持Linux），你可以使用这样的更新方式：

```shell
sudo apt update

sudo apt install modular
```

## 在Mojo playground中开发

除了下载Mojo SDK，你还可以在我们托管的Jupyter记事本Mojo Playground环境中实验Mojo。这是一个托管版本的[JupyterLab](https://jupyterlab.readthedocs.io/en/latest/)，运行的是我们最新的Mojo内核。


获取访问权限，通过[log in to the Mojo Playground here](https://playground.modular.com/)

![](https://docs.modular.com/static/images/mojo/mojo-playground.png)

## 预期

* Mojo Playground是一个JupyterHub环境，您可以在其中获得与您的帐户关联的私有卷，所以你可以创建你自己的记事本并对他们进行跨对话存储。

* 我们包含了一些记事本，向您展示Mojo的基础知识并展示其功能。

* 在云实例中vCPU核心数可能不同，所以集显性能不能代表语言性能。但是，正如您将在包含的```Matmul.ipynb```中看到的那样。Mojo相对于Python的性能是显著的。

* 这里可能有一些bug，请[report issues and feedback on GitHub](https://github.com/modularml/mojo/issues/new/choose)

## 贴士

* 如果你想保存对记事本的任何编辑，需要重命名文件。这些文件将会在服务器上刷新或更新。所以你重命名文件后，你的变更将是安全的。
* 你可以在记事本首行使用```%%python```后写标准python代码。在python单元中定义变量、函数和import可以在Mojo代码中访问。

## 警告

* 我们有没有提到包含的笔记本将丢失您的更改?

如果你想保存更改，重命名文件。

* Mojo环境没有网络权限，所以你不能安装其他工具或Python包。但是，我们包含了各种流行的Python包，比如```numpy```、```pandas```和```matplotlib```(查看如何[包含Python模块](https://docs.modular.com/mojo/programming-manual.html#python-integration))。

* 不支持重定义隐式变量（变量前面没有```let```或```var```）。如果你跨记事本模块重定义一个变量，你需要用var引入变量（```let```变量是不可变的）

* 你不可以在函数中使用全局变量-它只对全局变量可见。

* 列出一长串还不起作用或有痛点的事情，查看[Mojo roadmap and sharp edges](https://docs.modular.com/mojo/roadmap.html)