First of all you should know that it isn't that difficult to get your own server up and running with all of the tools provided by the CMaNGOS team. Once you have the necessary programs installed it takes about 10 minutes to compile the source code and start up a server. You don't need to be a programmer and you don't really need to be that tech savvy. As long as you can follow instructions and aren't afraid to ask questions on the forums, you will get there with no (major) problems.

首先你应该了解利用CMaNGOS团队提供的工具来建立自己的服务器并运行并不是什么难事.一旦你想进行,编译源代码并且运行大概需要10分钟的时间，并且你不需要是一个程序员或者懂得很多的大牛.你只需要按照指南里的命令或者去论坛里问一问，你可以找到你所要的一切帮助（当然不包含一些高深的问题）.

## Mangos... like the fruit?(Mangos... 有点像水果?)

Why is it called CMaNGOS? It is just a fun acronym that is easy to remember and say... like the fruit. Here is what it stands for:

C(ontinued) Ma(ssive) N(etwork) G(ame) O(bject) S(erver). The originating project was just called MaNGOS and so this is a "continued" version of the original.

为什么要叫它 CMaNGOS? 那只是为了容易记忆的首字母缩写... 是有点像水果. 到底代表着什么:

C(ontinued) Ma(ssive) N(etwork) G(ame) O(bject) S(erver). 原始项目叫做"MaNGOS","continued"代表着长久支持.

## What is git?(什么是GIT?)
Git is a source code revision control system and that's all you need to know about it for now (even though that may make no sense to you anyway). Github is the important thing to understand at the moment; it is a sort of social networking site for programmers and collaborators to share ideas and keep track of projects and it uses "git" to operate.

Git是一个源代码版本控制系统,这是你所知道的(尽管这可能对你来说没有任何意义).了解Github是一件很重要的事;它是一个使用"git"管理,程序员以及合作者分享想法和跟踪项目一个社交类网站.


Every time something is changed in the source code of a project it is tracked and recorded on Github. It also enables multiple people to work on their own versions of a project and then submit updates to the main version once they are perfected. Think of it like the project being a binder with a bunch of pages. If you wanted to, for example, add a new section to the binder, Github makes it so you can copy the whole thing and take it home with you to work on in your spare time. Then once you've finished adding the pages to your copy, you bring it back to the main project and suggest that the original project be updated with your changes. As you can imagine, this makes the whole process a lot easier to manage because you can have any number of people working on their own ideas without breaking the initial project.

每一次项目更改追踪信息都会记录在Github上.它还使多人能够在不同的版本下工作并向主要的版本上提交更新以完善主版本.它就像一个项目的多个页面的活页夹一样.如果想要,比如,添加新的部分到活页夹里.Github会制作和复制它们以便你可以在任何地方任何时间去修改它.一旦你修改好你的项目,
就可以将该修改带到主项目中并提交更改.可以想象,这使得这个过程变得更加容易管理，因为有许多对项目有不同想法的人实现不同的版本并且不会破坏原有的版本.

Github also has features to track issues with the code so that programmers can pickup various reported bugs, fix them, apply the fix to the main project, and then show that the fix was implemented.

Github还可以追踪问题，显示追踪程序的各种各样的BUG，并且解决这些问题，将他们修正到主要项目中，并且显示是如何修复这些BUG的.

## What are all these words?(这些词语是什么意思?)
There are a lot of terms ahead that you may not be familiar with so let's get started with some vocabulary:

有许多方面你可能还并不熟悉,所以先让我们来熟悉下这些词汇:

**Source Code** > Source Code is the basic foundation of programming; it is the actual code that is typed out by programmers in any of the thousands of different programming languages.

**Source Code** > Source Code(源代码)是编程的基础;它是程序员通过不同的编程语言编写的成千上万条实际代码.

**C++ or CPP** > Written both ways interchangeably, C++ (pronounced "see-plus-plus") is a programming language. Everything in CMaNGOS (except for the databases) is written in C++.

***C++ or CPP* > 两种书写方法都可以,C++(发音 "see-plus-plus") 是一种编程语言.CMaNGOS 主要是用C++编写(除了数据库).

**Server** > In a client-server relationship, the "server" is where information is stored. The server hosts an environment or database of information for clients to connect to and retrieve. In the context of CMaNGOS, "Server" could refer to many things such as the game server, the login server, or the database server.

**Server** > 在 client-server 的关系里,"server"是信息储存的地方.服务器主机的环境或数据库的信息通过客户端连接和检索.在CMaNGOS中,"Server"可以指很多东西如游戏服务器,登陆服务器,或者数据库服务器.

**Client** > In a client-server relationship, the "client" is where information is viewed. The client connects to the server and retrieves packets of information to display to the user. In the context of CMaNGOS, "Client" will always refer to the WoW game client that you have installed on your computer.

**Client** > 在 client-server 的关系里,"client"是阅览信息的地方.客户端连接到服务器并获取数据包的信息显示给用户.在CMaNGOS中,"Client"总是指安装在你电脑上的WOW游戏客户端.

**Repository** > If Github was a filing cabinet then a repository would be a single folder in said cabinet. Projects are referred to as "repos" in this world because you are basically referring to a folder with a bunch of source code in it.

**Repository(仓库)** > 如果Github是一个文件柜那么仓库就是放在它里面的文件夹.项目是被称为"repos"其实就是存放在文件夹里的源代码.

**Open Source** > Open source refers to the concept of everything being open and available to share with anyone. In the programming world, open source means that the code is openly shared and available to anyone to add to, edit, or copy as they wish (within the bounds of the respective terms of use).

**Open Source(开源)** > 开源的概念是指一切开放,可以与任何人分享.在程序世界里,开源意味着代码公开共享,任何人都可以添加,修改,以及复制(这些操作有可能遵循一些开源的使用条款).

**Compile** > When code is written it just looks like a bunch of text and symbols organized in strange ways that makes no sense to non-programmers. "Compiling" is the process of turning said code into a working program.

**Compile(编译)** > 编写代码时,对那些非程序员看起来就像一堆文本和符号以奇怪的方式组合在一起. "编译" 是说代码转变成一个工作项目的过程.

**Compiler** > Code doesn't compile itself and so we must use other programs to do it. These programs are called compilers.

**Compiler(编译器)** > 代码不能自己编译自己,所以我们需要编译工具.这些工具被称为编译器.

**Bug** > A bug is a term programmers use to describe problems with code. A bug is usually the culprit when a program you are using shuts down for no apparent reason or when something just doesn't work.

**Bug** > "Bug"是程序员用来描述一段有问题的程序的术语. "Bug"通常是一个程序无缘无故关闭或者无法工作的罪魁祸首.

**Database** > A database is a big heap of information typically organized in columns and rows much like an excel spreadsheet.

**Database(数据库)** > 数据库是一个行和列组织起来的大型堆形式数据.就像excel电子表格.

**SQL** > SQL is another programming language which stands for Structured Query Language and is used for managing databases.

**SQL(结构化查询语言)** > SQL是一个用来管理数据库的结构化查询语言.

**SQL Server** > An SQL Server is a virtual database (see above) that stores a bunch of stuff and uses the SQL language to operate.

**SQL Server** > SQL Server是一个用来储存数据的实际意义上的数据库服务，使用SQL语言操作.

**SQL Client** > Just because an SQL Server exists doesn't mean you can look at it like you would an excel sheet, at least not without another program. An SQL Client is a program that visualizes an SQL Server so that you can actually click and open things on the screen.

**SQL Client** > 仅仅因拥有一个SQL Server你还不能把它作为excel来使用, 至少得有另外一个程序. 一个SQL Client可以将SQL Server的信息展示在屏幕上,这样你就可以在屏幕上操作它.

**MySQL** > MySQL is a version of SQL that CMaNGOS uses. Continuing with the spreadsheet example, it would be like deciding to use Microsoft Excel vs Google Spreadsheet. Both basically do the same thing but have different interfaces, styles, and associated programs.

**MySQL** > MySQL是CMaNGOS使用的SQL版本. 继续Excel的例子, 就像你是喜欢微软的电子表格还是Google的电子表格一样. 双方都能做相同的事情,但又不同的风格和不同的工具.

**Query** > A query is a command being executed in SQL. When you update something on the server it sends a query just as when you pull information from the server it uses a query. Within the instructions, using a query will typically refer to entering a specific command into the command prompt or terminal you are using.

**Query** > 在SQL中意味一条命令的执行. 当你更新某条信息时候会创建一条Query,同样当从服务器拿某些信息的时候也需要一条Query. 在使用说明中,使用Query通常会引用一个特定的命令输入到命令提示符或终端使用。

## Step-by-step(循序渐进)
So from start to finish, this is a quick summary of the steps you will take to get a server running. You may not understand many (or any) of these yet but you have to start somewhere!

1. Download and install all the tools mentioned in the installation instructions (e.g. Git, Visual Studio, etc).
2. Download or install a WoW client and patch it to the proper version of the server you want to build (e.g. if you were building a Classic server you would need a WoW client patched to version 1.12.1).
3. Setup a MySQL Server.
4. Create a folder on your hard drive to place all of your work.
5. Copy the necessary repositories from Github to said folder.
6. Compile the source code.
7. Create and populate your MySQL Server databases.
8. Extract resources from your WoW client.
9. Move all necessary files and resources to your "run" folder.
10. Edit the configuration files.
11. Run realmd.exe.
12. Run mangosd.exe.
13. If updates are needed to your databases, apply them as needed and restart mangosd.exe.
14. Update your client's realmlist.wtf document to point to your server.
15. Run wow.exe and enjoy!

从开始到结束,你需要一台服务器来运行这些核心步骤.你可能有许多不明白(或是什么都不明白),但你必须从这里开始!

1. 下载和安装所有在安装说明中提到的工具 (例如:Git, Visual Studio等等).
2. 下载和安装你想建立的服务器版本对应的WOW游戏客户端和补丁(例如:比如你想要建立经典旧世的服务器,你可能需要下载一个1.12.1版本的WOW游戏客户端).
3. 安装并设置一个MYSQL服务器.
4. 在你的硬盘上建立一个文件夹以保存你的所有工作.
5. 从Github上下载所需服务器版本源代码.
6. 编译源代码.
7. 创建和更新你的mysql数据库.
8. 从你的WOW客户端提取资源文件.
9. 将所有提取的必须文件复制到编译后的"run"文件夹下.
10. 编辑配置文件.
11. 运行 realmd.exe.
12. 运行 mangosd.exe.
13. 如果需要更新数据库,需要根据情况重启mangosd.exe等程序.
14. 更新你客户端的realmlist.wtf文件指向目标服务器.
15. 启动 wow.exe 并开始享受游戏带来的快乐吧!

## Where do I start?(从哪里开始?)
The next sections of this guide will focus on all of the different pieces of CMaNGOS and how they work together. Remember that this guide will not tell you how to put them together, it will just give you a simplified explanation of what everything is. The Installation Instructions (found here) is where you should go for the actual process of building a CMaNGOS server.

本指南的下一个部分将关注CMaNGOS不同的部分以及它们是如何一起工作的.记住本指南不会告诉你是如何将他们放在一起的,它只会简单的解释这些东西.安装指南是你应该阅览的建立一个服务器的实际过程.

**Next**: [What Everything Is](https://github.com/cmangos/issues/wiki/Beginners-Guide-What-Everything-Is)

[新手指南主页](https://github.com/cmangos/issues/wiki/Beginners-Guide-Home)