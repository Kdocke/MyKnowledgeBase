# Snippet 博客主题配置

> Date: 2020-6-21
>
> Author: Kdocke
>
> Theme: hexo-theme-snippet

## 一、下载主题

Git 方式：进入 Hexo 博客所在主目录，执行：

```
git clone git://github.com/shenliyang/hexo-theme-snippet.git themes/hexo-theme-snippet
```

![git-download-hexo-theme-snippet](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/git-download-hexo-theme-snippet.png)

## 二、安装主题插件

因为 **hexo-theme-snippet** 使用了 `ejs` 模版引擎 、 `Less` CSS预编译语言以及在官方插件的基础上 进行功能的开发，以下为必装插件：

```
npm i hexo-renderer-ejs hexo-renderer-less hexo-deployer-git -S
或
cnpm install --save hexo-renderer-ejs hexo-renderer-less hexo-deployer-git
```

![install-theme-plugin](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/install-theme-plugin.png)

## 三、测试

1.修改 hexo-theme-snippet 为 snippet，然后更改站点配置文件的theme配置为snippet

![update-theme-conf-file-to-snippet](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/update-theme-conf-file-to-snippet.png)

2.然后执行下述命令，再访问浏览器，即可看到主题已经更换成功。

```bash
hexo clean #清空生成的静态文件
hexo g #生成新的静态文件
hexo s #开启本地访问
```

![local-test-snippet](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/local-test-snippet.png)

3.将博客推到 github, `hexo d`

![deploy-test-snippet](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/deploy-test-snippet.png)

## 四、菜单配置

### 1.修改页面菜单（分类）名称

修改博客主题目录下 `_config.yml` 文件中的 `menu` 项为以下内容：

```
## menu
menu:
- page: 主页
  url: /
  icon:
- page: 教程
  url: /categories/教程/
  icon:
- page: 记录
  url: /categories/记录/
  icon:
- page: 散文
  url: /categories/散文/
  icon:
- page: 时间轴
  url: /archives/
  icon:
```

若要添加新的菜单（分类），只需按照上述格式添加：

```
- page: 分享
  url: /categories/分享/
  icon:
```

### 2.修改新建文章模板

修改博客目录下 `scaffolds` 中的 `post.md` 内容为以下：

```
---
title: {{ title }}
date: {{ date }}
categories:
tags:
comments: false
img:
---
```

### 3.新建文章

为教程分类下新建一篇 `Node.js 安装教程` 的测试文章 hexo n "`Node.js 安装教程`"

编辑文章内容如下：

```
---
title: Node.js 的安装教程	// 文章标题
comments: true			   // 是否开启评论
date: 2020-06-22 11:45:29  // 文章日期
categories: '教程'		  // 文章分类
tags: ['Node.js', 'npm']   // 文章标签
img: https://nodejs.org/static/images/logos/nodejs-new-pantone-white.svg				  // 封面
---

## 下载

官网下载 | 镜像下载

---

## 安装

双击下一步安装

---

## 测试

cmd

---

## 参考

[官网]()
```

重新启动后，访问 教程 页面可以看到新建的文章

![menu-conf](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/menu-conf.png)

## 五、网站配置

**修改博客图标：**在 snippet 主题下，修改 souce 目录下的 favicon.ico 图标为自己的图标。

![ico-conf](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/ico-conf.png)

**修改博客标题及博客语言：**修改博客配置文件 `_config.yml` 中的 Site 为：

````
# Site
title: Kdocke
subtitle: ''
description: ''
keywords:
author: Kdocke
language: zh-CN
timezone: ''
````

![update-site-title](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/update-site-title.png)

**修改博客头像：** 修改博客主题下 `snippet\source\img\avatar.jpg` 头像为自己的头像。

**修改网站宣传语：** 修改博客主题下的 _config.yml 配置文件中的 branding 项为：

```
## 网站宣传语
branding: 生命在于折腾
```

**修改博客 head-img 图片：**修改博客主题下 `snippet\source\img\hea-img.jpg` 图片为自己的图片，并将其链接指向自己的博客，修改 博客主题 下的配置文件 _config.yml 的 Carousel 项：

```
## Carousel
carousel:
  img: './img/head-img.jpg'
  url: 'https://kdocke.github.io/'
```

## 六、创建 about 页面

在 Hexo 博客所在主目录，执行 `hexo new page about` :

![create-about-page](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Snippet博客主题配置/create-about-page.png)

此时会在 souce 文件夹下创建 about 文件夹，并且里面已经新建好了 index.md 文件。

新增 关于 的菜单选项，修改博客主题目录下 `_config.yml` 文件中的 `menu` 项，增加：

```
- page: 关于
  url: /about/
  icon:
```

修改 index.md：

```
---
title: 关于博主
date: 2020-07-13 11:15:50关于我
---

## 关于我
生命在于折腾

## 联系我
博主 Github 地址：https://github.com/Kdocke
联系邮箱：kdocked@163.com
```

重启 hexo 即可。

## 七、搜索配置

如果要使用本地站点搜索，必须安装插件hexo-generator-json-content来创建本地搜索json文件

```
npm i hexo-generator-json-content@2.2.0 -S
或
cnpm install --save hexo-generator-json-content@2.2.0
```

然后修改主题配置_config.yml文件下`jsonContent`相关参数。

```
## 搜索
jsonContent:
  searchLocal: true // 是否启用本地搜索
  searchGoogle: false //是否启用谷歌搜索
  posts:
    title: true
    text: true
    content: true
    categories: false
    tags: false
```

## 八、评论配置

 使用 [Valine—— 一款极简的无后端评论系统](https://valine.js.org/) 作为评论系统。

**1.获取 `APP ID` 和 `APP KEY`**

- 点击[登录](https://leancloud.cn/dashboard/login.html#/signup)或[注册](https://leancloud.cn/dashboard/login.html#/signup)`Leancloud`，注册需要实名;
- 创建应用
- 获取 APP ID 和 APP KEY: 刚刚创建的应用 > 设置 > 应用 KEY

**2.编辑博客主题的配置文件 _config.yml 的 Valine评论项**

```
## Valine评论
valine:
   enable: true
   appId: 自己的APP ID
   appKey: 自己的APP KEY
   placeholder: 说点什么吧
   notify: false
   verify: false
   avatar: wavatar
   meta: nick,mail
   pageSize: 10
```

配置中 avatar（头像） 默认为 mm，可以更改，有以下选项：

| 参数         | 备注                                                |
| :----------- | :-------------------------------------------------- |
| 空字符串`''` | Gravatar 官方图形                                   |
| `mm`         | 神秘人 (一个灰白头像)                               |
| `identicon`  | 抽象几何图形 (根据邮箱或昵称生成)                   |
| `monsterid`  | 小怪物                                              |
| `wavatar`    | 用不同面孔和背景组合生成的头像 (根据邮箱或昵称生成) |
| `retro`      | 八位像素复古头像 (根据邮箱或昵称生成)               |

