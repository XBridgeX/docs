# <center>XBridge-CSharp</center>

<center>与基岩版MC服务器的QQ远控</center>

***

## 装载

将XBridge.dll和XBridge.json放入MiraiNative的plugins文件夹即可

配置文件位于MiraiNative/data/io.XBridge.bds

```/wss/``` - WebsocketServer文件夹

```/logs/``` - 运行日志

```.lang``` - XBridge的语言文件

```die_id.json``` - 由玩家自身原因死亡的消息文件

```mobs.json``` - 生物命名表

```playerdata.xdb``` - 储存白名单，统计数据

```GroupData.json``` - 群聊设置文件

```Regex.json``` - 开启正则功能后会生成这个文件，可以自定义正则表达式

```setting.json``` - 主要配置文件，解析在[这里](https://gitee.com/DreamLition/XBridge/blob/master/SETTING/Setting.md)

## 使用

 - [基本使用](./user_cmd.md)

 - [命令系统](https://gitee.com/DreamLition/XBridge/blob/master/CMD/CMD.md)

 - [正则表达式](./regex.md)

 - [LUA](https://gitee.com/DreamLition/XBridge/blob/master/LUA/API.md)
