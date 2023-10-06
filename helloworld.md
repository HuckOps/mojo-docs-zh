安装完Mojo后，你可以使用[Mojo CLI](https://docs.modular.com/mojo/cli/)构建和编译Mojo程序。所以我们创建一个景点启动程序，打印“Hello， world!”

> ***开始之前***
> 你需要设置```MODULAR_HOME```和```PATH```环境变量，当你运行```modular install mojo```时输出描述。比如，如果你使用bash，你可以按照这样设置：
>```bash
>echo 'export MODULAR_HOME="$HOME/.modular"' >> ~/.bashrc
>
>echo 'export PATH="$MODULAR_HOME/pkg/packages.modular.com_mojo/bin:$PATH"' >> ~/.bashrc
>
>source ~/.bashrc
>```

如果你在安装的时候遇到其他问题，查看我们的[已知issues](https://docs.modular.com/mojo/roadmap.html#mojo-sdk-known-issues)

## 在REPL系统运行代码

首先，让我们尝试在Mojo REPL上运行一些代码，可以允许编写和直接在命令提示符里运行Mojo代码：

1. 启动一个REPL会话，在终端中输入```mojo```后按```Enter```键

2. 然后输入```print("Hello, world!")```后按```Enter```两次（必须使用一个空行表示表示一个表达式结束）

这里是一个例子：

```shell
$ mojo
Welcome to Mojo! 🔥

Expressions are delimited by a blank line.
Type `:quit` to exit the REPL and `:mojo help` for further assistance.

1> print("Hello, world!")
2.
Hello, world!
```

你可以在REPL中写更多你想写的代码。你可以按```Enter```键开始一个新行然后继续编写代码，如果你想让Mojo评估你的代码，按两次```Enter```。如果这里有一些打印，Mojo将会打印出来并返回提示给你。

REPL的主要用途是段表达式，因为代码不会被保存。所以如果你想写真正的程序，你需要把代码写入```.mojo```的源文件中。

## 编译和运行Mojo源码文件

现在，让我们在源文件中打印“Hello, world”。Mojo代码需要被定义成```.mojo```或```.🔥```扩展名。

你可以通过```mojo```命令行快速运行一个Mojo文件，你可以使用```mojo build```命令编译成可执行文件。让我们试试。

## 运行一个Mojo文件

首先，编写一个Mojo代码并运行它：

1. 创建一个文件名叫```hello.mojo```(或者```hello.🔥)并添加下边代码：

```mojo
fn main():
   print("Hello, world!")
```

这是你所有需要做的，保存代码后退出到命令行。

2. 现在使用```mojo```命令行运行它：

```bash
mojo hello.mojo
```

它会立刻打印消息：
```
Hello, world!
```

如果你的代码不工作，再次检查你的代码和第一步代码严格一致，并且确保你正确[安装Mojo](https://docs.modular.com/mojo/manual/get-started/#install-mojo)

## 编译一个可执行二进制文件

现在，编译和运行可执行文件：

1. 使用```build```命令创建一个独立的可执行文件：

```bash
mojo build hello.mojo
```

它将创建一个和```.mojo```文件同名的可执行文件，并且你可以通过```-o```选项改变名称。

2. 运行可执行文件：

```bash
./hello
```

可执行文件在系统上的运行方式和C或C++运行方式相似。

## 下一步

* 如果你在VS Code上开发，安装[Mojo extension](https://marketplace.visualstudio.com/items?itemName=modular-mojotools.vscode-mojo)，你可以获得语法高亮显示、编译、诊断等等。

* 如果你是Mojo新手，阅读[Mojo语言基础]().

* 如果你想打包你的代码成一个库，阅读[Mojo模块和包]。

* 如果你想展示一些Mojo代码，克隆我们的repo查看一些例子

    ```bash
    git clone https://github.com/modularml/mojo.git
    ```

    在你的IDE中打开我们例子的```/examples```目录：

    * [代码例子](https://github.com/modularml/mojo/tree/main/examples/)提供多种标准库demo帮助你学习Mojo特性和开始你自己的项目。

    * [Mojo notbooks](https://github.com/modularml/mojo/tree/main/examples/notebooks#readme)是和Jupyter notbooks相似的，我们在[Mojo Playground](https://playground.modular.com/)上发布，展示了多样的语言特性，现在使用Mojo SDK，你可以在VS Code或者JupyterLab上运行。

* 深入了解语言，阅读[Mojo程序设计手册](https://docs.modular.com/mojo/programming-manual.html)

* 查看所有Mojo可用的API，查看[Mojo标准库介绍](https://docs.modular.com/mojo/lib.html)
