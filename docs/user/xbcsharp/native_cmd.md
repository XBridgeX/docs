# <center>XBridge原生命令</center>


<center>在任意主群(Group.main)，具有管理员身份的群员均可使用```/xb run xxx```来执行XBridge命令</center>


***

## XBridge的白名单组件

> ```wl <string:mode> <string:arg1> [string:arg2]```

```wl add 1145141919 hhaaaaa``` - 添加QQ号为1145141919,xboxid为hhaaaaa的成员到XBridge白名单

```wl remove hhaaaaa``` - 从XBridge白名单移除xbooxid为hhaaaaa的成员的白名单

```wl list``` - 返回XBridge白名单列表

```wl get hhaaaaa``` - 取得xboxid为hhaaaaa的成员的QQ号

```wl get 1145141919``` - 取得QQ为1141541919的成员的xboxid

***

## XBridge的lua组件

> ```lua <string:arg1> <string:arg2>```

```lua run print('nmsl')``` - 返回一个"void",因为这个函数没有返回值

```lua run return "nmsl"``` - 返回"nmsl"

```lua call main``` - 调用lua虚拟机中的```main```函数，函数必须是注册过的

***

## XBridge的临时管理员

> ```admin <string:arg1> <int:arg2>```

出于安全考虑,用xb_console添加的管理员不会保存在配置文件之中

```admin add 1145141919``` - 添加QQ号为1145141919的用户到管理员列表

```admin remove 1145141919``` - 从管理员列表移除QQ号为1145141919的用户

***

## XBridge运行时临时配置

> ```setconfig <int:group> <string:type> <bool:arg>```

```setconfig 1145141919 chatenable false``` - 关闭群聊1145141919的服务器到群聊的聊天转发

```setconfig 1145141919 joinenable false``` - 关闭群聊1145141919的服务器到群聊的加入提示

```setconfig 1145141919 leftenable false``` - 关闭群聊1145141919的服务器到群聊的离开提示

```setconfig 1145141919 mobdieenable false``` - 关闭群聊1145141919的服务器到群聊的死亡死亡转发

```setconfig 1145141919 autowl true``` - 开启群聊1145141919的自助白名单

```setconfig 1145141919 chat chat{空格}``` - 设置群聊1145141919内聊天转发索引为```chat ```

 - 如果设置的前缀中具有空格，使用{空格}来替换

 - XBridge默认转发所有，设置索引后会只转发匹配项，如果想转发所有把索引设为```*```就可以

```setconfig 1145141919 chatsub 30``` - 将群聊1145141919的长度截取值设为30

 - 为了避免过长的群聊消息刷屏，XBridge默认截取前20位

```setconfig 1145141919 addserver 下北泽``` - 把名为“下北泽”的服务器加入群聊1145141919的白名单中

```setconfig 1145141919 removeserver 下北泽``` - 把名为“下北泽”的服务器移出群聊1145141919的白名单中

***

## ```reload```

> ```reload```

重载配置文件，包括正则，语言文件，lua