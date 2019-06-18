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
点击右下角的"?",勾选Edit Markdown.
输入以下内容
```
```
#Summary

* [Introduction](README.md)
* [第一章](chapter1/README.md)
* [第一节](chapter1/section1.md)
* [第二节](chapter1/section2.md)
* [第二章](chapter2/README.md)
* [第一节](chapter2/section1.md)
* [第二节](chapter2/section2.md)
* [结束](end/README.md)
```
```
    ![](/assets/gitbook_summary_1.PNG)

然后切换到项目目录下，打开命令行窗口，输入``` gitbook init```进行初始化，如果没安装gitbook,会自动安装gitbook，需要等待一段时间，安装完成后，开始初始化，初始化完成生成如下所示文件。
    ![](/assets/gitbook_init.PNG)

然后再输入``` gitbook serve```命令启动服务器，运行查看效果。
如果安装的是gitbook 2.3.2版本话报错，报错如下
    ![](/assets/gitbook_serve_err.PNG)
解决办法如下：
打开C:\Users\Administrator\.gitbook\versions\3.2.3\lib\output\website\copyPluginAsserts.js， 修改文件的112行,将confirm:true改为false。
    ![](/assets/gitbook_serve_sv.PNG)
再次运行，将启动服务器，如下所示
    ![](/assets/gitbook_serve_sc.PNG)
可以在浏览器中访问[http://localhost:4000](http://localhost:4000)进行访问。

关于图片,你可以在项目下创建assets文件夹将资源丢在assets文件夹中 然后可以多拽 或手动引入

##其他
其实还有更加方便的使用,就是你可以直接通过 gitbook editor 创建好项目后通过gitbook build或gitbook serve命令运行编译,后直接把编译好的目录下有个 _book 拷出来 放在自己的服务器上
