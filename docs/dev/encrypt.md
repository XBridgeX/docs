# <center>数据包加密</center>

<center>本页面会展示如何生成标准的加密数据包</center>

***

为了服务器安全考虑，KWO会强制发送和接收加密数据包，LLWS则可选加密/不加密

不过，二者的加密格式完全相同，您无需考虑兼容问题。

## 加密格式

 - 取密码大写MD5作为基密码
 - 前16位作为AES_Key
 - 后16位作为AES_IV
 - 使用AES/CBC/PCKS7Padding(PCKS5Padding理论上通用)

## 具体加密方法

比如现在我有一个未加密的标准包，向服务器执行list命令

``` json
{
    "type":"pack",
    "action":"runcmdrequest",
    "params":{
        "cmd":"list",
        "id":"114-514-1919-810"
    }
}
```

接下来我对这个数据包进行上文提到的AES加密

加密后的数据包如下所示

```
ewogICAgInR5cGUiOiJwYWNrIiwKICAgICJhY3Rpb24iOiJydW5jbWRyZXF1ZXN0IiwKICAgICJwYXJhbXMiOnsKICAgICAgICAiY21kIjoibGlzdCIsCiAgICAgICAgImlkIjoiMTE0LTUxNC0xOTE5LTgxMCIKICAgIH0KfQ==
```

现在，我生成一个新包，将加密过的内容填入```params```项的```raw```中，并在```mode```中填入加密格式

```json
{
    "type":"encrypted",
    "params":{
        "mode":"aes_cbc_pck7padding",
        "raw":"ewogICAgInR5cGUiOiJwYWNrIiwKICAgICJhY3Rpb24iOiJydW5jbWRyZXF1ZXN0IiwKICAgCJwYXJhbXMiOnsK"
    }
}
```

现在，一个标准的加密包就生成完毕了，您可以将它发送给KWO/LLWS。


