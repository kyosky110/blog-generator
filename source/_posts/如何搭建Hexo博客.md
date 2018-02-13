---
title: 如何搭建Hexo博客
date: 2018-02-13 11:24:39
tags:
---

## 简介
博客一般是程序猿总结(zhuang bi)的地方，所以就算我们不搭建，也至少要学会如何搭建。而Hexo配合github就是最方便的一种搭建博客的方式，至少可以节省很多时间来耍几把dota。

## 安装与使用篇
既然决定要搭建，首先就得先安装。

* Hexo之插件安装
  ```
  npm install -g hexo-cli
  ```
  在命令行输入上述代码就OK了，这是一切的成功之母，如果这一步完蛋了，那之后的不用看的。当然本人是不会在此详细说明各种错误的(gen ben bu hui jie jue)，如有问题请移步[此处](https://hexo.io/zh-cn/docs/index.html)。

* Hexo之博客初始化
  在终端输入下面内容
  1. `hexo init myBlog`

  2. `cd myBlog`

  3. `npm i`

  说白了上面的就是博客的初始化和依赖的下载，不懂也不要紧，跟着敲就行。

* Hexo之你的第一篇博客

  现在可以开始写博客文章了,输入下面命令

  1. `hexo new 文章来了`

  2. 在`source/_posts/`路径下可以看到有`文章来了.md`markdown文件，此时你就可以编辑内容了。

* Hexo之github仓库

  1. 在Github上创建一个空白的新仓库。

  2. 进入myBlog根目录打开`_config.yml`这个配置文件，在最后一行`deploy: type: `里面修改为下面的:
    ```
    deploy:
      type: git
      repo: git@github.com:xxx.git
      //repo是你的仓库命令
    ```
  3. Hexo之github与博客手牵手:命令行输入`npm install hexo-deployer-git --save` ，安装 git 部署插件.

  4. 去吧Github:命令行输入`hexo deploy`,这时就会把博客上传到github上。

  5. 在你github仓库的`Settings`打开Github page，这样就可以通过域名访问到你的博客了。

## 不好看？让我们换衣服吧(Hexo的主题切换)

到这儿是不是有满满的成就感呢，只不过页面太难看了，这时我们就得想办法变的酷一点(diao zha tian).

* 关于主题的[资源](https://github.com/hexojs/hexo/wiki/Themes)和文章网络上多得很，下面大致随便教一下.

* 首先进入根目录下的`themes`文件 `cd themes`。

* 然后下载资源。`git clone git@github.com:iissnan/hexo-theme-next.git` 或者根据各个资源的GitHub的教程来，比如最新的https://github.com/iissnan/hexo-theme-next 。

* 将_config.yml 的75行`theme:` 改为你下载的文件夹 比如 `theme: next`.

* 生成一下 `hexo generate`

* 去吧github `hexo deploy`，你可以根据你的github page观看了。


然后的然后就结束了(我要打游戏去了)。
