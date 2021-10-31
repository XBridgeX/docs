# <center>配置文件</center>
***

``` json
{ 
  "bdspath": "C:\\Users\\Lition\\Desktop\\bds\\bedrock_server_mod.exe",
  "wsport": 8080,
  "wskey": "password",
  "Encoding": "utf8",
  "wsenable": false,
  "autorestart": false,
  "Notargets": false
}
```

| 配置项   | 含义 |
| ----------- | ----------- |
|```bdspath```| 要启动的程序主路径|
|```wsport```|websocket服务器监听到端口|
|```wskey```| websocket密匙|
|```Encoding``` |控制台输出编码，可选```utf8```,```gbk```,```ascii```|
|```wsenable``` |是否开启websocket功能|
|```autorestart``` |是否自动重启服务器|
|```Notargets```| 是否忽略未找到目标的提示|
