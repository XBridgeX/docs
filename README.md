# XBridgeX | 文档中心
## 简介
XBridgeX文档中心页面由[mkdocs](https://mkdocs.org)生成。要维护本页面，您需要：

* 阅读mkdocs使用文档。详见 https://mkdocs.org;
* 熟悉Markdown语法

## 文档编写
请按照以下步骤进行操作：

1. 安装Python环境；
2. 部署mkdocs环境包、主题：
```python
pip install mkdocs
pip install mkdocs-material
```

3. 将本仓库克隆到本地：
```git
git clone https://github.com/XBridgeX/docs.git
```
4. 开始编写您的文档。

## 文档发布
1. 编写完成后，请先使用``mkdocs build``在本地生成静态页面进行测试；
2. 确保页面书写无误后，使用``mkdocs gh-deploy``将静态页面发布到Github；
3. 最后，将本仓库提交，并推送到Github。