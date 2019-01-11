本项目是 OBS Classic 的Android 远程控制端.
插件端代码参见  https://github.com/bilhamil/OBSRemote

现在OBS 软件用于直播,广告很火,因此有人想用手机来来遥控,因为obs支持插件机制,因此有人开发不少远程开源插件

目前obs软件分为两个版本, obs classic (经典版) 以及 obs stduio (工作室版), 前者用Visual Studio 开发,只能运行在windows上, 后面用 QT开发,能运行在Windows/Linux/Mac 上

https://github.com/jp9000/OBS  (classic 版已经停更了)
https://github.com/obsproject/obs-studio (Studio 版)

## 一. 经典版远程遥控方案

https://github.com/bilhamil/OBSRemote
这一版本插件是调用webSocket 来控制

手机端是用用Eclipse 开发原生控制程序
如果你只是测试手机端,不想用vs编译插件,可以直接下载编译好插件
http://sourceforge.net/projects/obsremote/files/OBS_Remote_1.1_ManualInstall.zip/download

把对应平台 WebSocketAPIPlugin.dll 直接放入obs插件目录即可.

则测试程序用Eclipse编译的,我现在升级到 Android Studio 具体代码参见
https://github.com/work4blue/obsremote

## 二. 工作室版本控制方案
这是针对Studio版本的插件源码
 https://github.com/Palakis/obs-websocket

对应测试的主要是一些脚本语言版本

*   Javascript (browser & nodejs): [obs-websocket-js](https://github.com/haganbmj/obs-websocket-js) by Brendan Hagan
*   C#/VB.NET: [obs-websocket-dotnet](https://github.com/Palakis/obs-websocket-dotnet)
*   Python 2 and 3: [obs-websocket-py](https://github.com/Elektordi/obs-websocket-py) by Guillaume Genty a.k.a Elektordi
*   Python 3.5+ with asyncio: [obs-ws-rc](https://github.com/KirillMysnik/obs-ws-rc) by Kirill Mysnik

其中https://github.com/haganbmj/obs-websocket-js 是用vue写的,
安装
> npm install obs-websocket-js --save
网页运行
> vue run dev

你可以用 HBuildler 构建成apk 在手机上运行.

打包方法
https://blog.csdn.net/museions/article/details/78960525

也可以参考经典来用原生来开发
