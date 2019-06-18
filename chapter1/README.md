# 环境搭建
##插件安装

开始之前我们需要先安装：

- nodejs

    前往[Node.js官网](/ https://nodejs.org/en/)，
    下载最新版LTS Nodejs windows系统安装包
    安装成功后再cmd窗体中输入node -v 查看是否安装成功。
    可参考这篇[安装教程](http://www.runoob.com/nodejs/nodejs-install-setup.html)。
- gitbook

    下载[GitBook Editor windows版](https://www.gitbook.com/editor/)
    安装成功后桌面会有个gitbook图标
    双击打开查看是否安装成功:
    ![](/assets/gitbook_login_1.PNG)
    点击下面的"Do that later",免登陆进入主界面。
    然后开始安装gitbook，在目录下运行cmd控制台，输入：
    `npm install gitbook -cli -g`
##配置gitbook目录
在GitBook Editor界面菜单中找到Change Library Path..来改变工作路径。
![](/assets/gitbook_Path.PNG)
##创建测试项目
比如创建项目test点击Confirm创建，可以看到如下界面。
   ![](/assets/gitbook_login.PNG)
创建成功后找到SUMMARY.md,注意创建成功后，生成两个文件，一个是README.md是对书籍的简单介绍，一个是SUMMARY.md是书籍的目录结构。
![](/assets/gitbook_summary.PNG)