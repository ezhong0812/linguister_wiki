现在你已经知道什么事Github,CMaNGOS是什么以及数据库的大概信息.希望你也明白了什么是realmd和mangosd应用程序.那么这些事物是之间是怎样联系在一起并且使你可以在自己的服务器上玩WOW的呢?我们继续往下看!

# 为什么要有这么多组件?
一个大型多人在线游戏是需要许多不同的组件并运行的.它不是简单的在你的本地计算机上玩,比如《模拟人生》和《天际》.为什么呢？因为这些游戏的信息都是储存在你的本地计算机中,不需要联网玩.它们在游戏内有自己的内置数据库而且仅仅只有一个玩家,只需要根据玩家所在的地图和房间来加载信息.在一个大型多人在线游戏中,无论如何,整个游戏世界总是运行着的,里面有许多玩家并且可以进行交流和互动.除此之外,游戏世界的许多变量不能保存在本地,因为：(1)过多的信息保存在客户端的话,黑客会利用这些信息,因为玩家是可以获取客户端的信息的.(2)在同一个游戏世界中需要对不同的玩家进行不同的响应.因此信息需要保存在一个中立的地方,否在如果存放在一个玩家本地中的话,当其游戏客户东不可用或断线其他的玩家将访问不到这些信息.所有这些都需要有一个"服务器"概念,并且许多"客户端"链接到它.

### 游戏服务器
游戏里所有范围内的事件都在mangosd.exe应用中运行.游戏服务器不仅管理服务器的物理环境,也管理非玩家以及NPC和生物的动作和事件,天气系统,游戏事件比如季节性的节日事件,和其他你想得到的在你游戏角色周边的事件.

### 客户端
wow.exe应用就是用来连接游戏服务器的客户端程序.

### 登陆服务器
你不能在没有登陆账号的时候链接一台服务器,所以我们需要在服务器中创建一个登陆账号. This is the realmd.exe application which also directs connecting clients to the realm that they want to play on after authenticating the player's login credentials.

### The Database
Even if we have a mangosd.exe and a realmd.exe running, there still needs to be a place to store the accounts and passwords and the objects and things in the game as well as the many variables associated with a single player; and so we have a third server called the database to store all of this information.


# How They Work Together
So you have your servers running and you are ready to try it out. You launch wow.exe...

The first thing that happens is the client attempts to find a login server at the location you told it to look: the address you entered into the realmlist.wtf document. Say you want the client to look for a login server on the same computer that you are running wow.exe: you would direct it to 127.0.0.1 (a universal address for your local computer to connect to itself). Because you have realmd.exe running, the client finds it and you are now ready to login. You type in some credentials and the server tells you that they are wrong, why? Because the login server needs to have your account stored somewhere in order to accept your credentials.

So now you switch over to your mangosd.exe application to create a new account. You type in the command "account create user password" which then adds a new account to the "realmd" MySQL database with the name "user" and the password "password."

You can now go back to your wow.exe client and type in the new credentials; the login server accepts your connection and allows you to select a realm to enter and begin playing. There will only be one available realm which by default is called "Mangos." You click on the realm and it loads the characters screen. Because this account was just created there are no saved characters so you create a new human warrior called "test" and enter the world.

As soon as you create test the human warrior, it is assigned an id number and all of the starting statistics, skills, abilities, and items are added to the "characters" MySQL database. Any time anything with the character changes, mangosd.exe will send an update to the MySQL database with the new information and save it there (character saves also occur at regular intervals in case the server crashes).

So you talked to the guard and moved around a bit and you are ready to start slaying some wolves. You target a wolf and right click to begin attacking. Because you are standing too far away the game tells you that you must move closer. You run up to the wolf and as soon as you are within range, you swing and take the wolf down to 50% health and it begins attacking you back. You may not realize it but a dozen processes and checks were just executed for that simple encounter.

1. **You right clicked on the creature**: the game server checked to see if you were in range by comparing your coordinates stored locally on the client to the coordinates of the creature stored in the "mangos" database. When it determined that you were not within range for a melee attack, it returned an error and a message that you are out of range (and probably played a bit of audio of your character saying something like "I'm out of range").

2. **You ran up to the wolf until you were in range**: your melee attack attempts to connect every few seconds (based on your weapon's attack speed) and so every time it tries to attack it checks your coordinates vs. your target's to see if you are in range. Because you were moving toward your target, the game repeated this check probably several times before it finally "passed" because you were in range.

3. **You hit the wolf and take it's health down by 50%**: so the game confirmed that you were in range and that you hit your target. It checked your weapon's attack damage against the wolf's defenses and randomly calculated an amount of damage based on those variables. It then subtracted that amount from the wolf's health.

4. **The wolf begins attacking you**: the wolf creature template is associated with a certain script which determines its behavior. Because this script tells it to defend itself, the game server directed the wolf to attack the hostile player hitting it.

Now let's say you want to create a guild. You travel to Stormwind and talk to the guildmaster dude to get a charter. You then get some friends to sign the charter (after of course managing to get your server setup so that other players can connect to it) and go back to the guildmaster. You submit your charter and voila... your guild is created. In that transaction mangosd.exe accepted input from the wow.exe client and then sent a command to the "characters" MySQL database to store: the name of the guild, the guild master, the tabard design and emblem, the various characters who are now members and their ranks, and a number of other variables.

As you can see, every little action and exchange of information is incredibly complicated and requires a lot of quick and efficient communication between the client and the multiple pieces of the server.

# Diagram of Client-Server Interactions
![](http://i.imgur.com/gYCNnGS.png)

## What's Next?
Now you can move on to the installation instructions and get started! Remember that the forums and the #cmangos IRC channel are full of people available to help you with any issues so don't be afraid to ask. Once you have a server up and running we encourage you to participate in the community, report bugs, and if you have some programming skills, try your hand at fixing or enhancing the repositories. There is plenty of information on the forums about how to participate and help out.

[Beginner's Guide Home](https://github.com/cmangos/issues/wiki/Beginners-Guide-Home)