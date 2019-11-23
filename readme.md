
# docker-php
> 快捷构建docker化nginx+mysql+php环境


### 快速部署
#### 1.下载
```shell
git clone https://github.com/fidding/docker-php.git ~/docker-php && cd ~/docker-php
```
#### 2.构建镜像
```shell
docker rmi docker-php;docker build -t docker-php php/.
```

#### 3.启动
```shell
docker-compose up -d
```

#### 4.demo演示
复制配置文件

```shell
cp demo/demo.conf ~/docker-data/nginx/conf.d && cp -rf demo/www/demo ~/docker-data/www
```
重启nginx

```shell
docker-compose restart docker-php
```
配置本地host

```shell
127.0.0.1   docker-php-demo.com
```

打开浏览器访问地址

[docker-php-demo.com](http://docker-php-demo.com)
    
---

## 介绍
### 关于环境
> 环境涉及nginx、mysql、php
#### nginx
- 容器名称: docker-nginx
- 端口: 90
#### mysql
- 容器名称: docker-mysql
- 端口: 3306
#### php/php-fpm
- 版本: 7.3
- 容器名称: docker-php
- 端口: 9000

### 关于目录
> 项目目录共分为两部分, 构建目录与数据目录
#### 1.构建目录
公开目录, 位于`~/docker-php`, 为docker-php源码目录, 涉及构建镜像版本与默认配置

```shell
~/docker-php
├── mysql
│   └── readme.md
├── nginx ng目录
│   └── readme.md
├── php php目录
│   ├── Dockerfile
│   └── readme.md
├── docker-compose.yaml
└── readme.md
```

#### 2.数据目录
个人目录, 位于`~/docker-data`, 为nginx、php、mysql配置与项目数据目录, 需注意安全性与保密性

```shell
~/docker-data
├── mysql mariadb环境目录
│   └── data sql数据目录
├── nginx nginx环境目录
│   ├── conf.d ng配置目录
│   └── log ng日志目录
├── php php环境目录
│   └── conf.d php扩展配置目录
└── www php代码项目目录
```

### 基本操作

#### compose操作 
操作需在docker-php项目目录下执行

1. 查看信息
    ```shell
    # 查看
    docker-compose ps 
    # 查看指定容器
    docker-compose ps <name>
    ```
2. 启动
    ```shell
    # 重启/启动/停止所有
    docker-compose restart/start/stop
    # 重启/启动/停止指定容器
    docker-compose restart/start/stop <name>
    ```
3. 日志
    ```shell
    # 查看所有
    docker-compose logs
    # 查看指定容器
    docker-compose logs <name>
    ```
