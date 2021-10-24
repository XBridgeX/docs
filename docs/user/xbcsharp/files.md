# <center>XBridge-CSharp</center>

<center>与基岩版MC服务器的QQ远控</center>

***

## 文件


配置文件位于`MiraiNative/data/io.XBridge.bds`

```/wss/``` - WebsocketServer文件夹

```/logs/``` - 运行日志

```.lang``` - XBridge的语言文件

```die_id.json``` - 由玩家自身原因死亡的消息文件

```mobs.json``` - 生物命名表

```playerdata.xdb``` - 储存白名单，统计数据

```GroupData.json``` - 群聊设置文件

```Regex.json``` - 开启正则功能后会生成这个文件，可以自定义正则表达式

```setting.json``` - 主要配置文件，解析在下面

***

## 主配置文件

``` jsonc
{
  "Servers": [ //服务器组
    {
      "name": "测试服", //服务器名称
      "Url": "ws://127.0.0.1:8801/mc",  //LLWS的url
      "password": "password",  //LLWS的密码
      "others":["空岛服"] //位于此列表中的服务器，会接收来自它们的跨服信息
    },
	{
      "name": "空岛服",
      "Url": "ws://127.0.0.1:8800/mc",
      "password": "password",
      "others":[] //留空则不会接收来自其他服务器的信息
    }
  ],
  "Group": {
    "main": [  //主群，用于获取白名单和执行命令
      952680774
    ],
    "chat": [  //聊天群，用于与服务器聊天
      952680774
    ]
  },
  "Admins": [  //管理员(们)
    2959435045
  ],
  "enable": {
    "xb_native": true,  //是否启用xb原生功能
    "xb_regex": true,   //是否启用正则表达式
    "xb_lua": true   //是否启用lua功能
  }
}
```

***

## 群聊设置文件

```jsonc
{
	"1145141919":{  //群号
		"chatenable":true,  //是否接收玩家聊天信息转发
		"joinenable":true,  //是否接收玩家入服信息转发
		"leftenable":true,  //是否接收玩家出服信息转发
		"mobdieenable":true,  //是否接收玩家死亡信息转发
		"allowserver":[  //服务器白名单，群聊只会接收来自白名单列表服务器的信息
			"空岛服",
			"生存服"
		],
		"errorenable":true, //错误信息是否发送到群聊，错误信息一般是ws收包解密失败或者是文件读取出错
		"chatindex":"*",  //聊天转发前缀
		"chatsub":20,  //聊天截取长度
		"autowl":true   //自助白名单是否开启
	}
}
```
非必要不需要更改此文件

使用XB原生命令可以直接更改设置

详见[原生命令](./native_cmd.md)