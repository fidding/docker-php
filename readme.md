
# docker-php
> 快捷构建php docker化

### 目录
#### 项目目录
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
#### 数据目录
```shell
~/docker-data
├── mysql
│   └── data sql数据目录
├── nginx ng目录
│   ├── conf.d ng配置目录
│   └── log ng日志目录
├── php php目录
│   └── conf.d php扩展配置目录
└── www 项目目录
```

### 构建与启动
#### 下载
```shell
# 下载镜像
git clone https://github.com/fidding/docker-php.git ~/docker-php
# 进入目录
cd ~/docker-php
```
#### 构建镜像
```shell
# php
docker build -t fidding/php-fpm php/.
```

#### 启动compose
```shell
&& docker-compose up -d
```

### compose操作 

1. 进入docker-php项目
    ```shell
    # 进入docker-php
    cd docker-php
    ```
2. 执行操作
    ```shell
    # 查看
    docker-compose ps 
    # 查看指定镜像
    docker-compose ps <name>
    
    # 重启/启动/停止所有
    docker-compose restart/start/stop
    # 重启/启动/停止指定镜像
    docker-compose restart/start/stop <name>
    ```