# openSUSE的折腾记录---软件篇

本篇文章是用来记录自己在openSUSE系统下，安装各种软件的经验、步骤等等，可能和别人的有类似，或者有些不正确的操作，但也都是个人的操作，只是为了记录下来，防止以后寻找不到，到时候用来参考查看，当然会持续的更新、修改、完善。

有想法、建议、更正的等等欢迎联系我，谢谢。

## 一、Chrome浏览器

openSUSE系统自带火狐浏览器，当然火狐也是一款非常好用的浏览器，但是也肯定不是一些人的首选，所以在这里安装Chrome浏览器。

首先需要到chrome浏览器的官网下载包   https://www.google.cn/chrome/index.html

下载后，找到包存放的文件夹，在文件夹内，右键-动作-在此处打开终端。
在终端中运行下列命令：

    sudo rpm -ivh google-chrome-stable_current_x86_64.rpm

等待运行成功后，即安装成功。在程序启动器中即可看到chrome浏览器。

## 二、网易云音乐播放器

新安装的系统中只有一个VLC，我们需要安装一个网易云音乐来听歌，嘿嘿，正常在官网是找不到网易云音乐的openSUSE的包，在openSUSE官网中找到了网易云音乐的包，但并不是所有人都可以在这里安装成功，所以使用终端安装，在终端运行以下命令：

    sudo zypper in netease-cloud-music

等待安装，安装成功后，在程序启动器中即可看到网易云音乐播放器。

## 三、VScode

VScode是一款很好的文本编辑器，可以安装各种插件来实现各种功能，这里我是为了在openSUSE系统下写markdown文档而下载，可以在VScode官网的文档中查看到openSUSE的安装步骤，依次在终端允许下列命令：

    sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
    
    sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/vscode.repo'

    sudo zypper refresh

    sudo zypper install code

安装完成后，在程序启动器中可以看到VScode。

打开VScode，进行一些基础的调试、设置，在扩展中搜索“Chinese”，安装中文插件，安装后，重启VScode，VScode变为中文。

在扩展中，搜索“markdown”，找到“Markdown All in One”和“Markdown Preview Github Styling”这两个扩展组件并安装组件，安装后，就可以在VScode中编写markdown文档了。

## 四、Arduino IDE

arduino是用来编写arduino开发板的一款IDE，首先需要在arduino官网下载包
https://www.arduino.cc/en/software

下载包到电脑后，解压缩包，在解压缩后的文件夹中，我们可以看到一个文件“install.sh”，运行该文件，即安装成功arduino IDE。

## 五、QT

安装QT用来开发学习。需要现在此连接下载软件包： http://download.qt.io/archive/qt/

这里我下载的是5.14.2版本的QT，所以下面运行命令的也是这个版本的，不同版本的包，需要运行不同的命令。

然后在终端运行下列命令：

    chmod +x qt-opensource-linux-x64-5.14.2.run

    su

    zypper install --type pattern devel_basis

    ./qt-opensource-linux-x64-5.14.2.run

运行最后一条命令后，弹出QT安装界面，安装之后，即可在程序启动器看到QT
