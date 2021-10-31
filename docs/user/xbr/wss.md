# <center>XBridgeR</center>

<center>websocket开发</center>

***

## WSS

XBridgeR内置了一个WEBSOCKET服务器，可以连接到XBridgeR来发送群聊信息

配置文件位于```io.Xbridge.bds/wss/setting.json```

``` json
{
    "enable":false, //是否开启websocket服务器，默认关闭
    "port":9395,    //服务器监听端口
    "endport":"/xbridge"
}
```
修改配置文件后重启XBridgeR

当在控制台出现如下字样时，代表websocket服务器开启成功

测试时使用的端口为9980，实际使用时会显示您设置的端口

```
[Info] Server started at ws://0.0.0.0:9980/xbridge (actual port 9980)
```

***

## 通信

### <center>消息包</center>

wss在发送群内收到的信息时，会把信息解析为消息包，如下是一个标准的消息包

```json
{
    "from":{
        "member":114514,  //发信者QQ号
        "xboxid":null,   //发信者XBOXID，没有记录为Null
        "group":1919810  //来源群
    },
    "messageChain":[
        {"type":"PlanText","text":"？"},  //纯文本
        {"type":"At","target":12345678},  //At某人
        {"type":"Image"},  //图片
        {"type":"AtAll"},   //At全体成员
        {"type":"Face","id":12} //小表情
    ]
}
```

***

### <center>发信息</center>

通过数据包同样可以发送信息到群聊

```json
{
    "action":"send",
    "params":{
        "target":114514,
        "text":"你好"
    }
}
```

这个包会向114514群聊发送你好