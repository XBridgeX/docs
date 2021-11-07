# <center>Nillauncher</center>

<center>启动参数</center>

***

|参数项|含义|默认值|
|::|::|::|
|-f|设置文件路径|./bedrock_server.exe|
|-p|websocket服务器端口|8080|
|-pwd|websocket密匙|password|
|-ep|websocket服务器endport|/mcws|
|-r|自动重启次数|5|

```
nillauncher.exe -p 8888 -pwd 114514
```

这个示例参数会设置websocket服务器端口为8888，密匙为114514

现在启动Bat

当控制台出现如下字样的时候，代表websocket服务器正常开启

注：测试时端口设置为8123，实际使用时会显示您设置的端口

```
[Info] Server started at ws://0.0.0.0:8123/mcws (actual port 8123)
```

