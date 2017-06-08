#### 安装：docker 17.03.1-ce
```
yum install -y yum-utils
yum-config-manager \
   --add-repo \
   https://download.docker.com/linux/centos/docker-ce.repo
yum makecache fast
yum -y install docker-ce
yum remove docker #删除
yum update docker #更新
```

#### 安装：docker-machine
让你轻松部署Docker实例到很多不同的平台。
 https://docs.docker.com/machine/install-machine/ https://github.com/docker/machine

```
curl -L https://github.com/docker/machine/releases/download/v0.12.0/docker-machine-`uname -s`-`uname -m` >/tmp/docker-machine &&
  chmod +x /tmp/docker-machine &&
  cp /tmp/docker-machine /usr/local/bin/docker-machine
```

#### 安装：docker-compose
```
 https://docs.docker.com/compose/install/  https://github.com/docker/compose
curl -L https://github.com/docker/compose/releases/download/1.13.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose &&
chmod +x /usr/local/bin/docker-compose

pip install docker-compose
```
#### MAC下安装

* MAC下安装：https://download.docker.com/mac/stable/Docker.dmg 下载后直接安装即可。然后再命令行访问。默认包含上面几个命令。
* VirtualBox安装

docker-Containerd
是Docker开源的众多项目中的新成员，这些项目包括libcontainer、libnetwork、notary、runC、HyperKit、VPNkit、Datakit、swarmkit和Infrakit等。


#### 配置daodocker镜像
* http://guide.daocloud.io/dcs/daocloud-9153151.html
curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://8cca9139.m.daocloud.io


#### 参考资源
* [Docker run执行流详解（以volume，network和libcontainer为线索）](http://blog.csdn.net/gao514916467/article/details/51201932)
* [理解Docker（3）：Docker 使用 Linux namespace 隔离容器的运行环境](http://www.cnblogs.com/sammyliu/p/5878973.html)
* [理解Docker（4）：Docker 容器使用 cgroups 限制资源使用](http://www.cnblogs.com/sammyliu/p/5886833.html)
* [docker 1.12 版本 docker swarm 集群](http://www.cnblogs.com/jicki/p/5611735.html)
* [docker深入2-熟悉v1.12](http://nosmoking.blog.51cto.com/3263888/1832212)

docker run -it  --rm --blkio-weight 100 --memory 10M --cpu-quota 25000 --cpu-period 2000 --cpu-shares 30 ubuntu:16.04 "/bin/bash"

####DOCKER命令：
systemctl start docker
docker --version/version/info
docker images
docker ps -al
docker run hello-world  / --help
docker inspect/rm/stop/start 91c95931e552

docker exec -it web31 ps -efdocker-machine ls

（1）docker swarm：集群管理，子命令有init, join, leave, update
（2）docker service：服务创建，子命令有create, inspect, update, remove, tasks
（3）docker node：节点管理，子命令有accept, promote, demote, inspect, update, tasks, ls, rm
（4）docker stack/deploy：试验特性，用于多应用部署， 类似与 docker-compose 中的特性。


总结：
docker machine：
内部ssh连接主机，自动部署docker。
创建本地虚拟的docker主机，或者云docker主机。
管理各个docker主机。
docker compose：
管理docker容器，协同调用。


#### docker-machine 测试
```
docker-machine create --driver virtualbox my-machine
docker-machine ls
docker-machine env my-machine
eval $(docker-machine env my-machine) 设置相关环境变量指向名为my-machine的虚拟机，后续docker命令都会远程的在这台虚拟机上执行。
docker-machine ip my-machine

#前提配置好ssh登陆，然后在root下。关闭防火墙，开放端口。
docker-machine create --driver generic --generic-ip-address=122.112.242.2 hwcloud-machine
docker-machine create --driver generic --generic-ip-address=59.110.234.196 aliyun-machine
docker-machine create -d none --url=tcp://59.110.234.196:2376 aliyun-machine
docker-machine create --driver generic --generic-ip-address=118.192.148.57 niaoyun-machine
docker-machine create --driver generic --generic-ip-address=13.58.196.13 aws-machine

docker $(docker-machine config aws-machine) run busybox echo hello world

docker-machine create --engine-registry-mirror=$ALI_MIRROR
```

#### docker swarm测试
##### 实例一
* [实战】Docker Machine + Compose + Swarm](http://dockone.io/article/275)
```
docker-machine create --driver virtualbox m1
#进入容器：
docker-machine ssh m1
docker run swarm create
#1a7b026359f18e4ddd3614b3d31ffc26

docker-machine create \
-d virtualbox \
--swarm \
--swarm-master \
--swarm-discovery token://1a7b026359f18e4ddd3614b3d31ffc26 \
swarm-master

docker-machine create \
-d virtualbox \
--swarm \
--swarm-discovery token://1a7b026359f18e4ddd3614b3d31ffc26 \
swarm-node1
```

##### 示例二
```
[leader机器]
docker swarm init --advertise-addr 192.168.99.100
docker node ls
docker service ls
docker node promote my-machine-node3 ( docker node demote my-machine-node3 降级)升级后node机器可以执行node service等命令
docker node rm vqhl8gv1yhjbd32mtkyp60egf

docker service create --name nginx --replicas 2 -p 80:80/tcp nginx
创建后 docker service ls 查看服务。docker service ps nginx 查看具体再哪几台运行。如果那个节点没有nginx镜像，会显示Preparing。你需要在节点上面docker pull nginx ，后就会自动启动。
docker service scale nginx=10
docker service ps nginx (docker ps -a)
对create后的服务，可以直接更改掉启动命令如：docker service update --replicas 3 --image nginx:new nginx
docker service rm nginx 的时候，所有的容器都会被 删除

docker service inspect --pretty nginx

docker node update --availability drain my-machine
docker node update --availability active my-machine

docker network ls

[node机器]
docker swarm join \
   --token SWMTKN-1-1k5y4awovd242yzk44vfc8ryrmxzi9gytfce4chh7g7589cjb8-7j4pl7dwbhobqaifuzd3ahivo \
   192.168.99.100:2377
swarm leave 后，manage上面显示为Down，然后执行： docker node rm vqhl8gv1yhjbd32mtkyp60egf 真实删除

```
