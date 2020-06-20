# 使用 Hexo 搭建个人博客

> Date: 2016-6-19
>
> Author: Kdocke
>
> Reference: [CodeSheep程序羊 Youtube 视频教程](https://youtu.be/erKYtw4Rfhk)

## 一、安装 Git

参考：[Git 安装教程](https://github.com/Kdocke/MyKnowledgeBase/blob/master/Tutorial/Git%20%E7%9A%84%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.md)

## 二、安装 Node.js

参考: [Node.js 安装教程](https://github.com/Kdocke/MyKnowledgeBase/blob/master/Tutorial/Node.js%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B.md)

## 三、安装 hexo

使用 cnpm 安装 hexo-cli

<img src="https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/install_hexo-cli-1.png" alt="install_hexo-cli-1"/>

验证 hexo 安装结果

![image-20200619153246580](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/install_hexo-cli-2.png)

## 四、本地简单使用

* 1.建立 `FirstBlog` 文件夹，并进入

* 2.在 `FirstBlog` 文件夹中初始化博客

  ![hexo-init](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/hexo-init.png)

* 3.安装后的文件

  ![inited-file](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/inited-file.png)

* 4.启动博客 `hexo s`

  ![start-blog-1](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/start-blog-1.png)

  ![start-blog-2](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/start-blog-2.png)

* 5.创建博文 `hexo n`

  ![create-first-blog](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/create-first-blog.png)

* 6.编辑并保存第一篇博文

  ![edit-first-blog](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/edit-first-blog.png)

* 7.清理 `hexo clean`

  ![hexo-clean](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/hexo-clean.png)

* 8.重新生成 `hexo g`

  ![regenerate-blog](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/regenerate-blog.png)

* 9.重新启动博客 `hexo s`

  ![my-first-blog](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/my-first-blog.png)

## 五、将博客部署到 GitHub

* 1.进入个人 GitHub，创建一个新仓库，注意仓库名的命名规则，需要自己的账号名 + github.io，后面需要用此仓库名来访问部署好的博客

  ![create-blog-repository](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/create-blog-repository.png)

* 2.安装 git 部署插件 `cnpm install --save hexo-deployer-git`

  ![install-hexo-deployer-git](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/install-hexo-deployer-git.png)

* 3.修改 Blog 目录下的 _config.yml 文件，将文件末尾的 deploy 项修改为以下内容

  ``` yml
  # Deployment
  ## Docs: https://hexo.io/docs/deployment.html
  deploy:
    type: git
    repo: https://github.com/Kdocke/Kdocke.github.io.git # 刚刚新建的仓库地址
    branch: master
  ```

* 4.开始部署 `hexo d`，中途会要求输入 github 的账号和密码，正常输入就可以

  ![deploy-github-finish-1](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/deploy-github-finish-1.png)

  ![deploy-github-finish-2](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/deploy-github-finish-2.png)

* 5.使用之前的仓库名访问部署好的博客网站

  ![success-access](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/success-access.png)

## 六、更换主题

主题地址：[hexo-theme-yilia](https://github.com/litten/hexo-theme-yilia)

* 1.安装 yilia 主题

  ```shell
  git clone https://github.com/litten/hexo-theme-yilia.git themes/yilia
  ```

  ![clone-yilia-theme](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/clone-yilia-theme.png)

* 2.修改 Blog 目录下的 _config.yml 文件，更改 theme 部分为以下内容:

  ```yml
  # Extensions
  ## Plugins: https://hexo.io/plugins/
  ## Themes: https://hexo.io/themes/
  theme: yilia
  ```

* 3.重新清理生成，`hexo clean` and `hexo g`

  ![re-clean-generate](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/re-clean-generate.png)

* 4.本地启动查看 `hexo s`

  ![yilia-local-start](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/yilia-local-start.png)

* 5.将博客推到 github，`hexo d`

  ![deploy-yilia-to-github](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/deploy-yilia-to-github.png)

* 6.访问

  ![access-yilia-blog](https://raw.githubusercontent.com/Kdocke/MyDocumentImg/master/MyKnowledgeBase/Tutorial/%E4%BD%BF%E7%94%A8%20Hexo%20%E6%90%AD%E5%BB%BA%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2/access-yilia-blog.png)