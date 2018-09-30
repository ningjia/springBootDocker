# Docker安装与常用命令
## 一、安装
参照：[CentOS Docker 安装](http://www.runoob.com/docker/centos-docker-install.html)

设置为开机启动
```
systemctl enable docker.service
```

## 二、常用命令
拉取docker镜像

```
docker pull image_name
```

查看宿主机上的镜像，Docker镜像保存在/var/lib/docker目录下:

```
docker images
```

删除镜像

```
docker rmi  docker.io/tomcat:7.0.77-jre7   或者  docker rmi b39c68b7af30
```

查看当前有哪些容器正在运行

```
docker ps
```

查看所有容器

```
docker ps -a
```

启动、停止、重启容器命令：

```
docker start container_name/container_id
docker stop container_name/container_id
docker restart container_name/container_id
```

守护态（后台）运行容器：

```
docker start -d container_name/container_id
```

后台启动一个容器后，如果想进入到这个容器，可以使用attach命令：

```
docker attach container_name/container_id
```

删除容器的命令：

```
docker rm container_name/container_id
```

删除所有停止的容器：

```
docker rm $(docker ps -a -q)
```

查看当前系统Docker信息

```
docker info
```

从Docker hub上下载某个镜像:

```
docker pull centos:latest
docker pull centos:latest
```

查找Docker Hub上的nginx镜像

```
docker search nginx
```

## 三、详细Docker教程：
[Docker基础教程及实践](https://blog.csdn.net/column/details/12885.html)
