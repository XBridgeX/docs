# <center>XBridgeR</center>


<center>常见问题</center>

***
<center>此处整理了已知可能出现的问题<br>
<font color="#FF0000">遇到bug，问题请先在此处寻找相关问题！</font><br>
任何问题先检查是否最新版本(看更新日志最新版本号)</center>


***

## Q：启动后弹窗报错

> A：你的配置文件写错啦！先检查你的json格式，如果没有问题，把报错的信息截图发到售后群，尝试寻找老用户为你解答

***

## Q：插件第一次修改配置文件后，服务器连接正常但是没有发送信息到群里

> A：去看看`io.Xbridge.bds/GroupData.json`的`allowserver`项中，服务器名称与配置文件是否匹配

***

## Q：为什么显示玩家进入服务器的次数都是0

> A：你的群员没有绑定xboxid，所以XBridgeR无法统计数据，用/bind命令绑定白名单即可

***

## Q：能不能更改一些xb_native的命令/回复？

> A：/bind，/unbind等命令在插件内部已经写死了，您可以通过正则表达式来自定义一些命令。回复的语句在.lang文件中可以自定义