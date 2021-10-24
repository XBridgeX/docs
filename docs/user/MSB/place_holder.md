# <center>MSerBot</center>

<center>新一代bds端机器人插件</center>

***

## 用户相关

|占位符|作用域|说明|
|--|--|--|
|qq_nick|群聊|发送者的QQ名字|
|qq_name_card|群聊|发送者的QQ名片
|qq_id|群聊|发送者QQ号|
|xbox_binding|群聊|发送者XBOX绑定状态(已绑定/未绑定)(true/false)|
|xbox_id|群聊|发送者绑定的XBOXID ⚠️非xuid|
|get_xboxid|群聊/控制台|指定用户的xbox名称 ⚠️仅在getXbox api后可用|

## 状态相关

|占位符|作用域|说明|
|--|--|--|
|cpu|群聊/控制台|	cpu占用百分比（取至小数点后一位）|
|total_memory_*type	|群聊/控制台|	总内存 ⚠️type可为bytes/kb/mb/gb|		
|free_memory_*type|群聊/控制台|可用内存 ⚠️type可为bytes/kb/mb/gb|
|used_memory_*types|群聊/控制台|已使用内存 ⚠️type可为bytes/kb/mb/gb|		
|memory_pert|群聊/控制台|内存使用百分比（取至小数点后一位）|	


## 时间相关


|占位符|作用域|说明|
|--|--|--|
|date	|群聊/控制台|	当前日期(yyyy-MM-dd)	|
|time	|群聊/控制台|	当前时间(HH:mm:ss)|	
|year	|群聊/控制台|	当前年份(yyyy)	|	
|month	|群聊/控制台|	当前月份(MM)		|	
|day	|群聊/控制台|	当前日期(dd)			|
|week	|群聊/控制台|	当前星期(EEEE)(星期X)|
|hour_12	|群聊/控制台|当前小时 *12小时制	|
|hour_24	|群聊/控制台|当前小时 *24小时制	|
|ampm	|群聊/控制台|	当前时段（am/pm）		|
|min	|群聊/控制台|	当前分钟			|
|secs	|群聊/控制台|	当前秒数		|	

## MotdBE相关


|占位符|作用域|说明|
|--|--|--|
|motd_name|群聊/控制台|获取到的服务器名字|		
|motd_protocol|群聊/控制台|获取到的服务器协议版本|					
|motd_version|群聊/控制台|获取到的服务器版本|	
|motd_gamemode|群聊/控制台|获取到的服务器默认游戏模式|
|motd_save|群聊/控制台|获取到的服务器存档名称|	
|motd_online|群聊/控制台|获取到的服务器当前在线|人数					
|motd_maxPlayers|群聊/控制台|获取到的服务器人数上限|					
|motd_difficulty|群聊/控制台|获取到的服务器默认难度|					