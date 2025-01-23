上周，OpenAI 发布了对话语言模型 ChatGPT，引发了全网热议。你是否也想亲自体验一番？本文将从开发环境准备、开发过程、服务器接口、腾讯 API 网关接入到部署，手把手教你如何开发一个 ChatGPT 微信小程序。

---

## 准备工作

### 1. 小程序申请

在微信中搜索 "ChatGPT" 相关的小程序，检查未被占用的名字。选定名称后，准备 144px*144px 尺寸的 logo，并在微信公众平台官网申请微信小程序。一般情况下，审核大约需要 3 个小时。

### 2. OpenAI 账号申请

访问 [OpenAI 官网](https://openai.com/) 申请账号。申请成功后，前往 [API 密钥页面](https://beta.openai.com/account/api-keys) 生成 `apiKey`，并妥善保存（密钥无法再次查看，丢失需重新生成）。

---

## 开发环境

### 1. 新建小程序

下载并安装 [微信开发者工具](https://developers.weixin.qq.com/miniprogram/dev/devtools/download.html)。建议选择基础模板并勾选微信云开发环境，以便快速了解小程序代码结构。

### 2. 环境介绍

小程序开发与传统的 HTML、CSS、JavaScript 开发网页类似。小程序的页面结构使用 `WXML`，样式使用 `WXSS`，逻辑和网络请求使用 `JS`。小程序包含一个描述整体程序的 `app` 和多个描述各自页面的 `page`。

---

## 开发过程

### 1. 引入 WeUI 组件

有两种方式引入 WeUI 组件：
- **通过扩展库引入**：不计入代码包大小。
- **通过 npm 下载构建**：包名为 `weui-miniprogram`。

如果希望快速实现效果，建议选择扩展库方式。参考 [WeUI 官方文档](https://wechat-miniprogram.github.io/weui/docs/quickstart.html)。

### 2. 定义 TabBar

在 `app.json` 中新增 `tabBar` 配置信息。注意 `tabBar-list-pagePath` 的路径必须存在，否则会报错。

### 3. 编写主界面

主界面包含一个输入框和一个询问按钮。用户点击按钮后，获取输入框中的值，向服务器的 `/ask` 接口发送请求，并将返回结果展示在页面中。

### 4. 绑定点击事件

在对应的 `js` 文件中定义 `submitForm` 方法，处理用户点击事件。

### 5. 请求服务器接口

在小程序后台的开发管理中配置服务器域名（需备案）。未配置域名时，可忽略域名强制检查进行调试，但正式上线时必须完成域名备案和配置。

---

## 服务器接口

为了快速开发，可以使用现有的 API 服务器脚手架（如 [template-node-egg](https://github.com/wytxer/template-node-egg)）。配置 `/ask` 接口，并在代码中使用 OpenAI 的 `apiKey` 进行请求。

---

## 腾讯 API 网关接入及部署

### 1. 网关接入

使用腾讯云 API 网关暴露接口到外网：
1. 访问 [腾讯云 API 网关](https://console.cloud.tencent.com/apigateway/service?rid=1)。
2. 新建服务，选择 HTTPS 协议。
3. 新建接口 `/ask` 并映射到服务器。

### 2. 部署过程

在微信开发者工具中上传代码，并在小程序后台查看上传版本。提交审核前，建议使用真机测试，修复可能存在的 Bug。审核通过后，可选择全量或灰度发布。

---

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)