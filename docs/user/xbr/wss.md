# <center>XBridgeR</center>

<center>与基岩版MC服务器的QQ远控</center>

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

施工中...
