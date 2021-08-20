---
sidebar: false
title: 快速部署 LaF 服务
---

### 快速部署 LaF 服务

> 基于 Docker Compose 快速部署，需要你熟悉 docker 以及 docker-compose 的使用

##### 安装 Docker  (CentOS)

> 本例只给出 CentOS 下的安装脚本，若安装其它环境请参考官方文档 https://docs.docker.com/engine/install/

```sh
sudo yum install -y yum-utils
sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo

sudo yum install docker-ce docker-ce-cli containerd.io
sudo systemctl start docker

```

> 还需安装 docker-compose @see  https://docs.docker.com/compose/install/

##### 启动服务

```sh
git clone https://github.com/Maslow/less-api-framework.git
cd less-api-framework

# 启动所有服务
docker-compose up

# 浏览器打开 http://locahost:8080 访问

```

##### 停止服务

```sh
# 停止服务
docker-compose down

# 停止服务并清数据卷
docker-compose down -v
```

##### 更新服务镜像

```sh
# 更新镜像
docker-compose pull
```