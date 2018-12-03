---
title: 使用Hexo+Github搭建属于自己的博客
date: 2018-12-03 14:29:14
tags:
---


##### 1、安装Node.js和配置好Node.js环境，打开cmd命令行，成功界面如下 

![微信截图_20181203112037.png](https://i.loli.net/2018/12/03/5c04a1569c914.png)

##### 2、安装Git和配置好Git环境，安装成功的象征就是在电脑上任何位置**鼠标右键**能够出现如下两个选择 

![微信截图_20181203112237.png](https://i.loli.net/2018/12/03/5c04a1dc2c277.png)

##### 3、Github账户注册和新建项目，项目必须要遵守格式：账户名.github.io，不然接下来会有很多麻烦。并且需要勾选Initialize this repository with a README 

![微信截图_20181203112924.png](https://i.loli.net/2018/12/03/5c04a35cc6ab3.png)

注意：必须选择一个主题才能访问github page

![微信截图_20181203114140.png](https://i.loli.net/2018/12/03/5c04c429b2f74.png)

在建好的项目右侧有个settings按钮，点击它，向下拉到GitHub Pages，你会看到那边有个网址，访问它，你将会惊奇的发现该项目已经被部署到网络上，能够通过外网来访问它。  

![微信截图_20181203135041.png](https://i.loli.net/2018/12/03/5c04c4b603ae5.png)

#####  4、安装Hexo，在自己认为合适的地方创个文件夹，如hello-hexo，然后通过命令行进入到该文件夹里面 

![微信截图_20181203135612.png](https://i.loli.net/2018/12/03/5c04c5ce42516.png)

输入npm install hexo -g，开始安装Hexo 

![微信截图_20181203135846.png](https://i.loli.net/2018/12/03/5c04c65963ef1.png)

进入到hello-hexo文件夹，点击右键，选择Git bash here，输入hexo -v，检查hexo是否安装成功 ![微信截图_20181203140327.png](https://i.loli.net/2018/12/03/5c04c7764cddf.png)

输入hexo init，初始化该文件夹（有点漫长的等待。。。） 

![微信截图_20181203140520.png](https://i.loli.net/2018/12/03/5c04c7e722606.png)

输入npm install，安装所需要的组件 ![微信截图_20181203140620.png](https://i.loli.net/2018/12/03/5c04c8223683f.png)

输入hexo g，首次体验Hexo ![微信截图_20181203140742.png](https://i.loli.net/2018/12/03/5c04c8740447f.png)

输入hexo s，开启服务器，访问该网址，正式体验Hexo 

![微信截图_20181203140839.png](https://i.loli.net/2018/12/03/5c04c8acae290.png)

![微信截图_20181203141023.png](https://i.loli.net/2018/12/03/5c04c91ba74a4.png)

问题：假如页面一直无法跳转，那么可能端口被占用了。此时我们ctrl+c停止服务器，接着输入“hexo server -p 端口号”来改变端口号 

![微信截图_20181203141306.png](https://i.loli.net/2018/12/03/5c04c9cd94072.png)

#####  5、将Hexo与Github page联系起来，设置Git的user name和email

进入到C盘-->当前用户-->.ssh，用记事本打开id_rsa.pub

![微信截图_20181203142112.png](https://i.loli.net/2018/12/03/5c04cb9e3a71f.png)

![微信截图_20181203142356.png](https://i.loli.net/2018/12/03/5c04cc40f3214.png)

登录Github，点击头像下的settings，添加ssh ![微信截图_20181203142012.png](https://i.loli.net/2018/12/03/5c04cb64a3e9d.png)

新建一个new ssh key，将id_rsa.pub文件里的内容复制上去 ![微信截图_20181203142501.png](https://i.loli.net/2018/12/03/5c04cc838eeb7.png)

##### 6、配置Deployment，在其文件夹中，找到_config.yml文件，修改repo值（在末尾） 

![微信截图_20181203142659.png](https://i.loli.net/2018/12/03/5c04ccf8b9c50.png)



##### 7、新建一篇博客，在cmd执行命令：hexo new post “博客名” 

![微信截图_20181203142954.png](https://i.loli.net/2018/12/03/5c04cdace0874.png)

这时候在文件夹_posts目录下将会看到已经创建的文件 

![微信截图_20181203143054.png](https://i.loli.net/2018/12/03/5c04cdea20d8d.png)



在生成以及部署文章之前，需要安装一个扩展：npm install hexo-deployer-git --save 

![微信截图_20181203143238.png](https://i.loli.net/2018/12/03/5c04ce4e846d8.png)

使用编辑器编好文章，那么就可以使用命令：hexo g，生成编译后的文件

![微信截图_20181203143417.png](https://i.loli.net/2018/12/03/5c04ceb00713d.png)

便以文件生成后，使用命令：hexo d，那么将看到生成的文章 ![微信截图_20181203144201.png](https://i.loli.net/2018/12/03/5c04d08273587.png)

部署成功后访问你的地址：http://用户名.github.io。那么将看到生成的文章 

![微信截图_20181203144140.png](https://i.loli.net/2018/12/03/5c04d0ea2838f.png)








