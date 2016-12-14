#Sublime中的git插件配置

##安装及配置

- 第一步：安装Sublime插件 `Git`，安装方法请上网查询，安装sublime插件的方法很多，在这里不说明了；

- 第二步：配置账号[访问](http://blog.csdn.net/itpinpai/article/details/53397539)

##使用方法
- 第一步：首先要有一个项目如： `git clone https://github.com/bxcn/sublime_pluginse`

- 第二步：通过sublime打开项目，在这个项目中添加几张图片；

- 第三步：`shift+ctrl+p`打开控制面板，输入`git add All`回车;
![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/add.png)

- 第四步：`shift+ctrl+p`打开控制面板，输入`git commit`回车后，打开个sublime的tab签，在第一行输入内容，这里的内容是 `git commit -m` 后面带的说明;

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/commit.png)

输入信息前

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/commit_message_before.png)

输入信息后

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/commit_message_before.png)

**注意:输入信息后，一定要关闭tab签**，然后会显示如图：

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/commit_message_print.png)


- 第五步：`shift+ctrl+p`打开控制面板，输入`git push Current Branch`回车;看到如下图片，说明上传成功

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/push.png)

![images](https://github.com/bxcn/sublime_plugins/blob/master/images/git/push_print.png)