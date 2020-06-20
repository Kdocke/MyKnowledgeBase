# Node.js安装教程

> Date: 2020-6-19
>
> Author: Kdocke
>
> Node.js-Version: 12.18.1
>
> Reason: 因为需要使用 npm 安装 Vue CLI，而 npm 是集成在 Node.js 中的，所以需要安装 Node.js

## 1、下载

访问官网：[Node.js](https://nodejs.org/zh-cn/)

<img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/nodejs-index.png" alt="Node.js首页" style="zoom:80%;" />

一般选择下载左侧的长期支持版本

## 2、安装

* 1.双击安装包

* 2.Next

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-1.png" alt="install-1" style="zoom: 80%;" />

* 3.同意协议

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-2.png" alt="install-2" style="zoom:80%;" />

* 4.选择安装位置，建议安装在 D 盘

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-3.png" alt="install-3" style="zoom:80%;" />

* 5.这里运行环境、npm 包管理器、在线文档快捷方式、添加到环境变量四项全部安装

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-4.png" alt="install-4" style="zoom:80%;" />

* 6.不用勾选，直接 Next

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-5.png" alt="install-5" style="zoom:80%;" />

* 7.install

  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/install-6.png" alt="install-6" style="zoom:80%;" />

* 8.等待安装完成，安装完成后会有两个组件
  * Node.js 本身
  * npm 包管理器

## 3、验证

打开 cmd，分别输入 `node --version` 和 `npm --version`, 如果正确输出版本号，证明安装成功

<img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/res.png" alt="res" style="zoom:80%;" />

## 4、设置依赖包安装路径

* 1.在 `nodejs` 安装目录下创建 `node_global` 以及 `node_cache` 文件夹

  ![rely-1](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/rely-1.png)

* 2.在 `nodejs\node_modules\npm` 设置 npmrc文件，使用文本文档打开修改里面的配置

   ```
  prefix=D:\bProgramSoftware\nodejs\node_global
  cache=D:\bProgramSoftware\nodejs\node_cache
  ```

  ![rely-2](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/rely-2.png)

* 3.设置环境变量，在 “系统变量” 中新建

  变量名为 `NODE_PATH`，

  变量值为  `D:\bProgramSoftware\nodejs`（变量值是自己 node 安装的根目录）

  之后在 “系统变量” 的 path 中新建两个变量 `%NODE_PATH%\node_modules` 和 `%NODE_PATH%\node_global`
  <img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B/rely-3.png" alt="rely-3" style="zoom:80%;" />

## 5、安装淘宝镜像

```shell
npm install -g cnpm --registry=https://registry.npm.taobao.org
```

