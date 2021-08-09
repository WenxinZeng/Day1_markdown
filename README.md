# Day1_markdown

# Mac安装java及环境配置

## Step 1: 安装jdk

JDK安装

1.访问Oracle官网 http://www.oracle.com，浏览到首页的底部菜单 ,然后按下图提示操作:
https://images2015.cnblogs.com/blog/877813/201601/877813-20160113135011647-96008710.png![image](https://user-images.githubusercontent.com/88622247/128668541-c424bf88-6cf7-48f6-9ce7-ebdf2809d957.png)


2.点击“JDK DOWNLOAD”按钮：

3.选择“Accept Lisence Agreement”同意协议:

4.点击Mac OS X x64后面的下载链接：

下载完成后点击安装包，按提示即可完成安装。

5.打开Finder,可以在下图所示的路径中找到安装好的jdk 1.8.0_40.jdk:



6.其中Contents下的Home文件夹，是该JDK的根目录。



其中：

bin目录下存放JDK用于开发的一些终端命令工具。常见的工具如：

“javac”的作用是将java源文件编译为class文件(即自解码文件)；

“java”命令的作用是运行class文件。

db目录下是java开发的一个开源的关系型数据库；

include目录下是一些C语言的头文件；

jre目录下JDK所依赖的java运行时；

lib目录下存放JDK开发工具所依赖的一些库文件；

man目录下存放JDK开发工具的说明文档。

然后输入”java -version”，如果看到jdk版本为1.8则说明配置已经生效：

 

环境变量配置



1、在英文输入法的状态下，按键盘“Ctrl + 空格”组合键，调出Spotlight搜索，在这里可以快速启动终端，输入ter,然后回车，即可打开终端：





2.如果你是第一次配置环境变量，可以使用“touch .bash_profile” 创建一个.bash_profile的隐藏配置文件(如果你是为编辑已存在的配置文件，则使用"open -e .bash_profile"命令)：



3.输入“open -e .bash_profile”命令：



4.输入如下配置：

JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_40.jdk/Contents/Home
PATH=$JAVA_HOME/bin:$PATH:.
CLASSPATH=$JAVA_HOME/lib/tools.jar:$JAVA_HOME/lib/dt.jar:.
export JAVA_HOME
export PATH
export CLASSPATH

然后保存关闭该窗口。



5.使用"source .bash_profile"使配置生效

6.输入 echo $JAVA_HOME 显示刚才配置的路径


# Git安装、clone、push
