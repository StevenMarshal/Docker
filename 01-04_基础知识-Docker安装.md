## 1.4 Docker安装

Docker的安装很简单，在linux系统上通过简单的几行命令就可以完成Docker的安装。

我们介绍Centos7上Docker的安装，Centos7系统的CentOS-Extras库中已经带了Docker，可以直接使用yum 命令安装

    yum install docker

安装之后启动Docker服务，并让它随系统启动自动加载。

    systemctl start docker.service
    systemctl enable docker.service

在命令行输入docker

![](images/1-4dockeranzhuang.png)
