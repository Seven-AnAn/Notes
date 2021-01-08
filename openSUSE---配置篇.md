# openSUSE的折腾记录---配置篇

本篇记录opensuse系统下，使用某些软件、功能时需要进行的一些配置操作，当然，也只是记录自己的配置过程，可能在某些操作、配置上有错误，请不要介意。

如果有想法、建议、更正等等欢迎联系我，谢谢。

## 一、QT创建项目

自己使用QT5来创建编写项目，并且使用的是cmake，而opensuse中没有，需要自己安装，在终端在运行以下命令安装：

    sudo zypper install bison ccache flex gcc gcc-c++ gcc-java gcc-info zlib-devel nasm boost-devel gsl-devel sqlite3-devel libqt4-devel libqt4-devel-doc cmake cmake-gui autoconf autogen automake automoc4 make qt-creator git mercurial

运行命令并安装结束后，打开QT创建cmake项目即可成功。