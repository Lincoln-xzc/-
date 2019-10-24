--
title: 如何快速开发一个小程序
date: 2019-10-20
tags:
---
# 如何快速开发一个小程序
小程序，即用即退，无需下载的方式得到了广大用户的喜好，那么我们就来学习如何快速的开发一款
自己的小程序。如果之前没有了解过小程序开发的前期准备工作的小伙伴，可以先上微信开发者社区看小程序开发文档，具体的我在这里就不多说了。文档写的很详情，如何注册账号，去哪里下载开发
者工具都有明确的说明。(https://developers.weixin.qq.com/miniprogram/dev/framework/quickstart/getstart.html#%E7%BC%96%E8%AF%91%E9%A2%84%E8%A7%88)
1.注册完账号，记住我们的AppId,这个在创建项目的时候需要填。
2.安装好微信开发工具，我们就开始创建我们的第一个小程序。

![image](https://github.com/Lincoln-xzc/-/blob/master/images/create.png)
#### 一. 小程序框架介绍和运行机制 
打开微信开发者工具，然后点击创建新项目。选择“普通快速启动模块”,然后整个项目目录如下，我这边引入了weui。

![image](https://github.com/Lincoln-xzc/-/blob/master/images/project.jpg)

接下来我们来介绍一下小程序的主要项目文件。
1. app.js
整个项目的启动文件，里面有onLaunch, globalData两个方法。
    onLaunch：小程序初始化完成时触发，全局只触发一次，我们可以把获取
用户登录成功的回调，用户的相关信息，获取缓存之类的相关操作写在这里。
    globalData：是定义整个项目的全局变量之类的，全局的变量可以在里
定义，后面再每个页面可以通过app.globalData来调用。
    onError: 小程序发生脚本错误或者API调用报错时都会触发。
![image](https://github.com/Lincoln-xzc/-/blob/master/images/app.jpg)
2. app.json
整个项目的配置文件，常用的配置项有：pages、window、tabBar.
   pages:页面路径列表，这里写的第一个文件路径，也是小程序默认的第一个展示页面。
   window: 全局的默认窗口配置
   tabBar: 底部tab栏的配置
 ![image](https://github.com/Lincoln-xzc/-/blob/master/images/setting.jpg)
3. pages
小程序的页面组件，有几个页面就有几个文件夹，创建page的时候有生成对应的js、json、wxss、wxml文件。
page.js里面对应着这个组件的声明周期，自定义的方法。跟vue/react很像。我们可以在这里写入组件对应的逻辑，需要渲染的数据。
page.json 组件的配置文件
page.wxml 组件的dom结构
page.wxss 组件的样式
#### 二. 小程序调试
   我们本地开发好的小程序，如果需要进行真机调试，在我们可以点击上面的预览或者上传，但是只有拥有体验权限的人才能在自己的微信里面使用。我们在微信公众平台上-项目成员添加对应体验人的微信，这样他就能体验的二维码在手机上面试用你开发的小程序了。
![image](https://github.com/Lincoln-xzc/-/blob/master/images/tiaoshi.jpg)
#### 三. 效果展示
##### 首页
![image](https://github.com/Lincoln-xzc/-/blob/master/images/home.png)
##### 分类
![image](https://github.com/Lincoln-xzc/-/blob/master/images/type.jpg)
##### 个人中心
![image](https://github.com/Lincoln-xzc/-/blob/master/images/index.jpg)
##### 个人信息编辑
![image](https://github.com/Lincoln-xzc/-/blob/master/images/edit.jpg)

    

  


