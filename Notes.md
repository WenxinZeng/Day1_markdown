# Day1_markdown

# Mac安装java及环境配置



## Step 1: 安装jdk



1.访问Oracle官网 http://www.oracle.com，浏览到首页的底部菜单 ,点击下图处:

![img](https://images2015.cnblogs.com/blog/877813/201601/877813-20160113135011647-96008710.png)2.点击“JDK DOWNLOAD”按钮：

![img](https://images2015.cnblogs.com/blog/877813/201601/877813-20160113135051835-861363050.png)3.选择“Accept Lisence Agreement”同意协议:

![img](https://images2015.cnblogs.com/blog/877813/201601/877813-20160113135219866-685515947.png)4.点击Mac OS X x64后面的下载链接：

![img](https://images2015.cnblogs.com/blog/877813/201601/877813-20160113135306585-54248836.png)下载完成后点击安装包，按提示即可完成安装。

5.打开Finder,可以在下图所示的路径中找到安装好的jdk 1.8.0_40.jdk:

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416153110191-1153954158.png)

6.其中Contents下的Home文件夹，是该JDK的根目录。

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416153449941-591903183.png)



然后输入”java -version”，如果看到jdk版本为1.8则说明配置已经生效：

 

**环境变量配置**

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416170843160-212359895.png)

1、在英文输入法的状态下，按键盘“Ctrl + 空格”组合键，调出Spotlight搜索，在这里可以快速启动终端，输入ter,然后回车，即可打开终端：

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416163814332-1190356067.png)

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416163825379-734294736.png)

2.如果你是第一次配置环境变量，可以使用“touch .bash_profile” 创建一个.bash_profile的隐藏配置文件(如果你是为编辑已存在的配置文件，则使用"open -e .bash_profile"命令)：

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416164957082-1418925235.png)

3.输入“open -e .bash_profile”命令：

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416165627113-2136824168.png)

4.输入如下配置：

JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_40.jdk/Contents/Home
PATH=$JAVA_HOME/bin:$PATH:.
CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.
export JAVA_HOME
export PATH
export CLASSPATH

然后保存关闭该窗口。

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416170310316-1801751113.png)

5.使用"source .bash_profile"使配置生效



## Step 2: 安装Eclipse





1.访问eclipse官方首页http://www.eclipse.org/home/index.php ，点击右上角“Download”按钮:

 2.选择一个镜像站点下载到Mac的桌面：

3.解压安装包，并将解压出来的Eclipse拖入Finder的应用程序中：

4.运行Eclipse,第一次运行时会让你设置工作空间workspace的位置，设置在文稿下即可。至此，已经成功安装了Eclipse。

5.打开Eclipse的偏好设置，我们需要对Eclipse做一下配置：

6.从左侧栏选择java下面的Installed JREs,然后点击Add按钮，我们要为Eclipse配置JDK：

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416223348707-544986165.png) 

 

7.Add JRE界面中点击JRE home后面的那个“Directory”按钮，选择安装JDK时的Home文件夹路径(参考 Mac下如何安装JDK 中的第5和6步)：

![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416224347691-322038548.png) 



11.勾选新增的JRE，点击右下角的Apply按钮，应用该配置：

 ![img](https://images2015.cnblogs.com/blog/877813/201604/877813-20160416224347691-322038548.png)



完成了Eclipse的配置.


## Step 3: Git 克隆及push

mac 命令行输入open ~/ .ssh，打开id_rsa.pub文件中的内容，复制到github->settings，选择SSH and GPG keys，new SSH key，新建，任意输入一个名称，把复制内容加在下面保存即可。

2：从github上的仓库中克隆代码

1
git clone git@github.com:name/vue-music.git　　
等待下载即可，过程中可能会遇到输入密码的问题

1
Enter passphrase for key '/Users/name/.ssh/id_rsa
我当时是用邮箱生成的，输入当时输入的密码即可，在命令行输入的过程中密码不会显示出来，输入完毕回车。

// 命令行输入 git status 查看修改的内容
git status
// 输入git branch，查看本地当前分支
git branch
// 输入git branch -a，查看所有的分支情况
git branch -a
// 输入git add .，把所有文件添加到仓库，git add src/components/login/login.vue，将login.vue文件添加到仓库中
// 输入git commit -m '修改login.vue文件'，git commit，将文件提交到仓库，-m 后面跟上提交的说明
git commit -m '修改login.vue文件'
4：pull远程分支到本地进行对比

git pull
5：push本地修改到远程分支

git push
6：在react中使用Ant Design Pro时，commit时经常因为eslint检查不过关，导致commit提交失败。

通过跳过eslint的代码检查

或者在项目里新建个.eslintignore文件，用来忽略检测的文件夹

git commit --no-verify -m "commit"
 

 

在把本地新建代码添加到指定代码仓库时的操作：

 

1：初始化版本库

git init

 

2：添加文件到缓存区

git add .

 

3：把添加的文件提交到版本库

git commit -m '提交到版本库'

 

4：本地代码关联远程代码仓库

git remote add origin 你的远程代码仓库地址

 

5：第一次推送到远程仓库

git push -u origin master


