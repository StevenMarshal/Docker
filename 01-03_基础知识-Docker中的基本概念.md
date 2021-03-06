## 1.3 Docker中的基本概念

Docker中包括三个基本概念：
* 镜像（Image)  
* 容器（Container)
* 仓库（Repository)  

理解好这三个概念，就可以了解Docker的整个生命周期。

镜像：  
是一个只读的模板，例如一个完整的Centos操作系统镜像可以用来创建Docker容器，Docker中提供了一个很简单的方式来创建镜像和更新镜像，甚至可以从其他地方直接拷贝已经做好的镜像直接使用。  
镜像有点类似于编程中的Class类，在运行的时候生成对象。

容器：  
是从镜像创建并运行的实例，就像一个启动好了的播放器程序，它可以被开始，停止，启动和删除。每个容器都是相互隔离的，绝对保证安全。
你可以把容易看成一个启动了的Liunx简化版系统，里面包括root用户权限，进程空间，用户空间和网络空间，还包括运行在里面的应用程序。

仓库：  
是集中存放镜像文件的地方。还有一种服务叫做仓库注册服务器（可以理解为GitHub这样的托管服务器），里面存放着多个仓库，每个仓库中又包含多个镜像，每个镜像又有不同的标签。仓库的概念有点类似于Git,也分为公有仓库和私有仓库，全世界最大的Docker仓库是Docker Hub,国内最大的Docker仓库是Docker Pool。  
用户可以在本地网络或者服务器上创建一个私有仓库，当用户创建了一个自己的镜像之后，使用push命令把镜像上传到自己的仓库中，下次在另外一台机器上使用这个镜像的时候，只需要从仓库中pull下来就可以直接使用了。
