# XBridgeN：概述
![GitHub](https://img.shields.io/github/license/XBridgeX/XBridge-Nodejs) ![GitHub forks](https://img.shields.io/github/forks/XBridgeX/XBridge-Nodejs) ![GitHub contributors](https://img.shields.io/github/contributors/XBridgeX/XBridge-Nodejs?color=orange) ![GitHub last commit (branch)](https://img.shields.io/github/last-commit/XBridgeX/XBridge-Nodejs/dev) ![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/XBridgeX/XBridge-Nodejs?include_prereleases)

**XBridgeN** 是XBridgeX项目下的一个群服互通机器人，基于[OICQ](https://github.com/takayama-lily/oicq)机器人框架、Node.js平台进行构建。
目前，XBridgeN已支持与主流的**WebSocket服务器***进行对接：

WebSocket服务器|类型|项目状态
--|--|--
[Nillauncher](https://github.com/XBridgeX/nillauncher)|BDS启动器软件|活动，开发中
[LLWebSocket（原BDXWebSocket）](https://www.minebbs.com/resources/c-bdx-liteloader-bdswebsocketapi.2150/)|BDS端基于LiteLoader平台的插件|活动
XWebSocket|BDS端基于CSR平台的插件|停更，已转向KWO

**WebSocket服务器***：泛指能够实现WebSocket通信的组件。这些组件通常以插件或者软件的形式存在。
<br><br>**阅读本文档，您将能够：**

* 掌握XBridgeN的基本使用

* 掌握XBridgeN的一般配置和高级配置