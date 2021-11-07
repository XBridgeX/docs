# <center>标准数据包</center> 
<center>nillauncher采用websocket进行通讯，本页面会介绍通讯使用的标准数据包</center>

***

## <center>📤 Nillauncher发出的数据包</center>

***

### 玩家加入服务器

✌️ player join

``` json
{
    "type":"pack",
    "cause":"join",
    "params":{
        "sender":"lition",
    }
}
```

### 玩家离开服务器

👋 player left

``` json
{
    "type":"pack",
    "cause":"left",
    "params":{
        "sender":"lition",
    }
}
```

### 玩家聊天

💬 player chat

``` json
{
    "type":"pack",
    "cause":"chat",
    "params":{
        "sender":"lition",
        "text":"哼哼 啊啊啊啊啊"
    }
}
```

### 执行命令返回


``` json
{
    "type":"pack",
    "cause":"runcmdfeedback",
    "params":{
        "result":"执行命令返回",
        "id":"执行时传入的id"
    }
}
```

### 服务器开启

``` json
{
    "type":"pack",
    "cause":"server_start",
    "params":{}
}
```

### 服务器进程退出

⚠️ 此处退出代表进程退出，如果用Bat启动程序则可能程序依旧在后台运行

``` json
{
    "type":"pack",
    "cause":"server_stop",
    "params":{}
}
```

### 直接发送文本

``` json
{
    "type":"pack",
    "cause":"plantext",
    "params":{
        "text":"哼哼 啊啊啊啊啊啊",
    }
}
```

### 调试信息


``` json
{
    "type":"pack",
    "cause":"debug",
    "params":{
        "msg":"此处返回信息不固定，作为描述使用",
    }
}
```

### 数据包解析失败

``` json
{
    "type":"pack",
    "cause":"decodefailed",
    "params":{
        "msg":"描述文本",
    }
}
```

## <center>📥 Nillauncher可接收的数据包</center>

***

### 向服务器发送文本消息

``` json
{
    "type":"pack",
    "action":"sendtext",
    "params":{
        "text":"要向服务器中发送的文本",
        "id":"此项无用"
    }
}
```

### 执行命令

``` json
{
    "type":"pack",
    "action":"runcmdrequest",
    "params":{
        "cmd":"要向服务器中执行的命令",
        "id":"返回执行结果时需要附带执行id"
    }
}
```

### 开启服务器

```json
{
    "type":"pack",
    "action":"startrequest",
    "params":{
        "id":"xxxx-xxxxxxxx-xxxxxxxxx-xxxxxxxx"
    }
}
```

### 关闭服务器

```json
{
    "type":"pack",
    "action":"stoprequest",
    "params":{
        "id":"xxxx-xxxxxxxx-xxxxxxxxx-xxxxxxxx"
    }
}
```

此数据包等同于向服务器执行stop命令

### 强制结束服务器进程

```json
{
    "type":"pack",
    "action":"serverkill_request",
    "params":{
        "id":"xxxx-xxxxxxxx-xxxxxxxxx-xxxxxxxx"
    }
}
```

非必要条件不推荐使用