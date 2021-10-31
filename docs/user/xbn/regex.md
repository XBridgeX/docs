# XBridgeN：高级配置
## 正则表达式
正则表达式是XBridgeN的核心功能。

文件位置|说明
--|--
`/config/regex.json`|配置群消息自动应答规则。


一个正则表达式配置文件的基本结构包括 **regex（正则体）**、**permission（所需执行权限）**、**actions（动作组）**。而**actions**内可以包含一个或多个动作。当玩家在群内发送消息时，如果发送的文本和正则表达式中配置中的关键词匹配，且玩家权限与该段关键词的所需权限匹配，即可触发相应的动作。

XBridgeN包含了默认的正则表达式配置，涵盖了大部分的功能。用户也可以对正则内容进行修改，满足各种使用场景的需求。下面将会针对默认的正则表达式配置文件进行详细介绍。

### 自助绑定白名单

```json
{
	"regex": "^绑定 ([A-Za-z0-9 ]{4,20})$",
	"permission": 0,
	"actions": [
		{
			"type": "bind_whitelist",
			"content": "白名单申请已发送，请等待管理员审核！",
			"whitelist_already_apply": "你已经申请过白名单了，请勿重复提交！"
		}
	]
}
```

![00](../../img/xbn/bind_whitelist.png)

### 自助解绑白名单

```json
{
	"regex": "^解绑$",
	"permission": 0,
	"actions": [
		{
			"type": "unbind_whitelist",
			"content": "解绑成功！",
			"player_not_bind": "无需解绑：你还没有绑定！"
		}
	]
}
```

![01](../../img/xbn/unbind_whitelist.png)

### 查询本人绑定状态

```json
{
	"regex": "^关于我$",
	"permission": 0,
	"actions": [
		{
			"type": "bind_check_self",
			"content": "我的信息：",
			"player_not_bind": "请先绑定白名单！"
		}
	]
}
```

![02](../../img/xbn/check_bind_self.png)


### 为目标玩家添加白名单

```json
{
	"regex": "^加白名单 (.+$)",
	"permission": 1,
	"actions": [
		{
			"type": "add_whitelist",
			"content": "已将该玩家添加到所有服务器的白名单!",
			"whitelist_already_add": "该玩家已经绑定，且已添加过白名单过了！",
			"player_not_bind": "该玩家未绑定，无法为其添加白名单！"
		}
	]
}
```

![03](../../img/xbn/add_whitelist.png)


### 删除目标玩家的白名单

```json
{
	"regex": "^删白名单 (.+$)",
	"permission": 1,
	"actions": [
		{
			"type": "del_whitelist",
			"content": "已将该玩家从所有服务器的白名单中移除!",
			"player_not_bind": "无需删除白名单：该玩家未绑定！"
		}
	]
}
```

![04](../../img/xbn/del_whitelist.png)

### 查询目标玩家的绑定状态

```json
{
	"regex": "^查绑定 (.+$)",
	"permission": 0,
	"actions": [
		{
			"type": "bind_check",
			"content": "查询结果：",
			"player_not_bind": "该玩家未绑定，未查询到任何信息！"
		}
	]
}
```

![05](../../img/xbn/check_bind.png)

### 执行服务器控制台指令（以“查服”为例）

```json
{
	"regex": "^查服$",
	"permission": 0,
	"actions": [
		{
			"type": "runcmd",
			"content": "list"	//指令内容
		}
	]
}
```

![06](../../img/xbn/runcmd.png)

### 发起异步http GET请求（以“百度”为例）

```json
{
	"regex": "^百度$",
	"permission": 0,
	"actions": [
		{
			"type": "http_get",
			"content": "http://www.baidu.com",	//请求地址
			"succeed": "百度一下，你就知道",	//请求成功时发送的群消息内容
			"failed": "请求失败,请检查网路"		//请求失败时发送的群消息内容
		}
	]
}
```

![07](../../img/xbn/http_get.png)

### 自动应答群消息（以“帮助”为例）

```json
{
	"regex": "^帮助$",
	"permission": 0,
	"actions": [
		{
			"type": "group_message",
			"content": "[Tokiame Bot 帮助信息]...（省略一万字）"
		}
	]
}
```

![08](../../img/xbn/group_message.png)
