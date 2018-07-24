## 1.3 Dockerfile的基本结构

Dockerfile 是一个文本格式的配置文件，用户可以使用Dockerfile快速创建自定义的镜像。

Dockerfile文件分为四个部分：  

* 基础镜像信息    

在Dockerfile中使用#完成一行的注解  
\#第一行必须制定基础镜像

    FROM centos

* 维护者信息
  
\#维护者信息  

    MAINTAINER your_name your_email

* 镜像操作指令
\#镜像操作指令，使用yum 安装mysql  

    RUN yum -qqy install mysql  

当然这些指令还有包括ADD、ENV、EXPOSE等

* 容器启动执行指令  

    CMD ["python","app.py"]

每运行一条RUN指令，镜像则添加新的一层，最后的CMD指令，制定容器启动时要启动的命令。
