# docker
>source：https://www.runoob.com/docker/docker-tutorial.html
>换源，略
## 容器(主动获取镜像 docker pull imagename，如果使用时主机没有，会自动下载)
1. 运行 
- docker run 镜像名 命令(/bin/bash)
- +参数
  - t 指定终端
  - i 交互
  - d 后台运行(默认不进入容器)
  --name 设定名字
- 退出 ctrl+D/exit
2. 常见命令
- 查看(所有)容器 docker ps (-a)
- 关闭容器 docker stop id
- 重启容器 docker restart id
- 进入容器 exec(退出后容器不停止)
- 导出容器快照到本地文件 docker export id > imagename.tar
- 快照导入为镜像 cat docker/imagename.tar | import - name 
- 删除容器 docker rm -f id;清理所有终止的容器 docker container prune(-f表示强制执行)
------
- 运行web应用 #-P 将容器内使用的网络端口随机映射到我们使用的主机上，-p 设置端口
example：用Python Flask 运行一个web应用 
```
docker pull training/webapp #默认端口为5000
docker run -d -P training/webapp python app.py 
docker run -d -p 2154:5000 training/webapp python app.py 
```
- 查看端口 docker port id/name 
- 查看日志 docker logs id/name
- 查看进程 docker top
- 查看配置和状态信息 docker inspect
- 启动用start，重启用restart
3. 
- 网络端口映射：容器的 -p 可以同时绑主机的ip和port,默认绑tcp端口，但可改 如：127.0.0.1:2001:5000/udp
- 连接容器：
 - 容器命名
 - 新建网络 docker network create -d bridge test-net(-d 确定docker网络类型，overlay用于swarm mode)
 - 加入网络 运行容器时添加 --network test-net(可用ping检验，多容器连接可用dockercompose)
 4.宿主机的daemon.json可以配置全部容器的dns，没什么用略了
## 镜像
1. 列出本机镜像 docker images(不指定镜像版本标签，默认下载最新版。ubuntu:16.04)
2. 查找镜像 docker search imagename
3. 删除镜像 docker rmi imagename
4. 更新镜像 可以按容器打包为镜像，更新容器，暂时用不到，不写了
5. 构建镜像 
- 先创建Dockerfile
- docker build -t imagename .(指定绝对路径的目录)
6. 设置镜像标签 docker tag id imagename:tagname
## 仓库
默认docker hub
docker login
docker logout
docker search
docker pull
docker push 
> Dockerfile的写法，yml文件的配置，虚拟机上安装docker的dockermachine，
>还有集群管理工具swarm暂时用不到，用时再看也不晚
