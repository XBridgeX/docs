# 开始使用XBridgeN
## 环境要求
* 主流的操作系统平台（包括但不限于Windows、Linux、MacOS）；
* 操作系统需要安装Node.js环境，且Node.js版本要求为14.x及以上

## 初始化配置与使用
1. 安装 [Node.js](https://nodejs.org/)（要求Node.js版本为14.x及以上）；
2. 下载 [XBridgeN](https://gitee.com/xbridgex/XBridge-Nodejs/attach_files/868764/download/XBridgeN_1.0.0_beta11012343.zip)；
3. 解压，然后进入XBridgeN目录，运行`run.bat`（Windows用户）或`run.sh`（Linux用户）,启动XBridgeN（如果启动时提示缺少依赖模块，请删除`node_modules`文件夹，在终端输入 `npm i` 重新安装依赖模块）。初次启动后会在``./config``目录下生成默认的全局配置文件，并自动退出；
4. 打开全局配置文件`/config/global_setting.json` ，根据实际情况进行修改：
```json
{
	"qq": 123456,   //机器人QQ账号
	"login_qrcode": true,  //是否使用扫码登录，默认为true。如使用密码登录，请改为false
	"use_protocol": 2,	//设置QQ登录协议。1:安卓手机 2:安卓平板 3:安卓手表 4:MacOS 5:iPad
	"qq_password": "qqpassword",  //机器人QQ密码。仅在"login_qrcode"为false（使用密码登录）时，该项配置才有效
	"ws_address": "ws://127.0.0.1:8080",    //Websocket服务端地址
	"ws_password": "wspassword",    //WebSocket通信密钥，请与WebSocket服务端通信密钥保持一致
	"qq_group": [
		"123456"   //QQ群号，目前暂时只支持一个QQ群
	],
	"server_name": "生存服务器",  //服务器名称，目前暂时只支持一个服务器
}
```

5. 再次启动XBridgeN，然后启动任意一个WebSocket服务端；
6. 当控制台出现以下类似的提示时，说明机器人配置无误且运行正常：
```
WS服务器连接成功！
[2021-10-21T15:54:18.496] [MARK] [iPad:123456] - 正在探索可用服务器...
[2021-10-21T15:54:18.551] [MARK] [iPad:123456] - connecting to 109.244.168.25:8080
[2021-10-21T15:54:18.595] [MARK] [iPad:123456] - 109.244.168.25:8080 connected
[2021-10-21T15:54:18.973] [MARK] [iPad:123456] - Welcome, abc ! 初始化资源...
[2021-10-21T15:54:19.205] [MARK] [iPad:123456] - 加载了1个好友，1个群，1个陌生人。
[2021-10-21T15:54:19.349] [MARK] [iPad:123456] - 初始化完毕，开始处理消息。
```