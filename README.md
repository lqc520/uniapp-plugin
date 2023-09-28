Uniapp插件开发



> 感谢您的关注和支持！如果您喜欢我的插件并想要支持我，可以通过微信赞赏码进行赞赏。您的每一份赞赏都是我更新更好内容的动力。也可以通过[好评](https://plugins.jetbrains.com/plugin/21470-uniapp-tool/reviews)来激励我！

> 个人能力和精力有限 不是每一个需求都能解决 会优先处理赞赏用户的需求 优先处理bug 提issues请按模板提问 不按模板提问有可能会直接被我关闭 谢谢！


## 最新版下载

[Uniapp插件下载](https://ghproxy.com/https://github.com/lqc520/uniapp-plugin/releases/download/v1.0.9-231.2/Uniapp-1.0.9-231.2.zip)

## 插件介绍

### 正式版
[![插件版本](https://img.shields.io/jetbrains/plugin/v/21470.svg)![插件版本](https://img.shields.io/jetbrains/plugin/d/21470.svg)](https://plugins.jetbrains.com/plugin/21470-uniapp-tool/versions)

### 功能

*   最新版本下载[ releases](https://github.com/lqc520/uniapp-plugin/releases)
*   插件市场下载 [uniapp tool](https://plugins.jetbrains.com/plugin/21470-uniapp-tool)
*   [使用说明](https://plugins.jetbrains.com/plugin/21470-uniapp-tool/readme)
*   Bug[ 提交](https://github.com/lqc520/uniapp-plugin/issues)
*   一款免费的 Uniapp插件 可以编译运行HbuildrX创建的uniapp项目
*   启动项目需要再后台  设置->工具->Uniapp->设置HbuilderX安装根目录
*   如需启动小程序      设置->工具->Uniapp->设置微信开发者工具安装根目录
*   支持编译运行vue2/vue3项目
*   支持rpx、upx、easycom 组件
*   支持uniapp的内置组件语法提示
*   支持对非cli项目的@/~路径识别、cli项目可以自行配置
*   支持创建页面、包路径自动注册、支持分包路径
*   支持发行微信小程序到官方后台
*   支持uniapp的条件编译、代码块折叠、高亮
*   支持文件androidPrivacy.json、manifest.json、pages.json 语法提示
*   支持创建uniapp cli项目 支持创建vue2项目\vue3项目\vue3-ts项目
*   支持运行uniapp子项目\子项目代码提示
*   支持分包路径跳转\代码提示\跳转

## 常见问题

### 如何配置路径

#### win配置

![win](https://plugins.jetbrains.com/files/21470/2121-page/dc681f77-fb9f-4e56-9015-f03f308d475b)

#### mac配置

 /Applications/HBuilderX.app/  

>要配置自己的项目的实际路径

### 如何使用插件创建创建cli项目

#### 创建vue3项目

![image-20230827213525022](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/27-1.png)

> degit和克隆差不多 如果使用有问题可能是github访问受限制、和插件无关 [官网文档](https://uniapp.dcloud.net.cn/quickstart-cli.html)

#### 创建vue2项目

![image-20230827213850706](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/27-2.png)

> 选中第二个cli就行 不用管理下方的vue3选项  并且会提示选择项目模板 [官网文档](https://uniapp.dcloud.net.cn/quickstart-cli.html)

### 如何使用分包功能

```
#pages.json添加以下结构 root路径可以自定义 在项目那边新建页面可以识别到subPackages参数 可以新建分包页面并且注册到pages.json 
"subPackages": [
    {
      "root": "pages/xxx",
      "pages": []
    }
  ]
```

### 如何使用微信发行到官方后台功能

先使用hbx执行一遍 [使用教程](https://hx.dcloud.net.cn/cli/publish-mp-weixin?id=uploadPrivateKey) 后续可在webstorm配置参数 直接发行 

### 插件支不支持子模块

目前插件支持子模块功能 目前仅支持一个子项目  有多个子项目的需求提issues

### 插件支不支持编译其他类型项目 比方说快手啥的

可以支持 有需要提issues 



## 版本变动

### v1.0.9

- 支持css emmet
- 优化解析manifest文件
- 优化创建页面添加记忆功能
- 优化rpx支持（ws2023.2.2版本官方已经支持rpx/upx 低版本继续支持，高版本使用官方支持）

### v1.0.8

- 创建cli项目
- 支持运行子项目\子项目代码提示
- 支持分包路径跳转\代码提示
- 支持微信小程序上传查看日志
- 支持动态配置插件部分功能 兼容一些性能较差的设备
- 分包页面创建优化 微信小程序配置key路径优化
- 整体代码提示功能优化 页面路径跳转优化 支持在pages.json 点击分包root 选中目录等

### v1.0.7

- 生命周期函数优化
- 路径跳转优化
- 支持xml emmet

### v1.0.6

- 支持生命周期函数提示
- 优化cli项目取消路径识别（自行配置路径别名）
- 支持条件编译高亮
- 支持小程序编译时压缩代码

### v1.0.5

- 分包问题修复
- 条件编译折叠
- 支付宝、抖音编译发行（不自动打开工具、因为还是需要手动导入项目）
- image属性src添加jpg、png文件路径提示(后续改成和img提示一样)

### v1.0.4

- vue3项目运行

- 条件编译

- 页面url路径识别

- 分包注册

- rpx upx 全局支持


### v1.0.3

- [#4](https://github.com/lqc520/uniapp-plugin/issues/4)
- 借助uni-helper对androidPrivacy.json、manifest.json、pages.json 文件语法支持和提示
- 新建页面注册到pages.json 目前仅支持主包
- pages.json 中的路径识别
- 微信小程序发行到微信官方后台（请先用hx走一遍）
- 语法支持加强

### v1.0.2

- 适配mac适配

### v1.0.1

- 支持easycom

### v1.0.0

- 支持运行网页、微信小程序
- 支持发行网页、小程序
- 支持启动微信小程序
- sass、less环境下支持rpx upx
- ~/@ 识别为项目路径







## 使用教程

本工具依赖于hx需要配置安装的根目录

![image-20230408181904355](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/image-20230408181904355.png)

启动项目

![1681358169857](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/1681358169857.png)



语法提示 路径识别

![01](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/01.gif)



注册页面

![02](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/02.gif)

内置组件支持加强

![03](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/03.gif)

路径提示

![04](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/04.gif)

上传到微信官方后台

![05](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/05.png)

emmet

![emmet](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/50.gif)



## 感谢

插件开发借鉴了不少开源项目比如wechat-mini-program-support elemen 插件官方项目、uni-helper等



## 支持

![1681358169857](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/zs.jpg)

感谢您的关注和支持！如果您喜欢我的插件并想要支持我，可以通过微信赞赏码进行赞赏。您的每一份赞赏都是我更新更好内容的动力。谢谢您的支持！

## 联系

> 加我微信注明来意

![联系我](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/user.jpg?x-oss-process=image/resize,w_300,limit_0) ![群聊](https://wldmy.oss-cn-shenzhen.aliyuncs.com/fjdmy/img/group.jpg?x-oss-process=image/resize,w_300,limit_0)


