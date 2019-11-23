
# docker-php
> 快捷构建docker化nginx+mysql+php环境


### 构建与启动
#### 下载
```shell
# 下载镜像并进入目录
git clone https://github.com/fidding/docker-php.git ~/docker-php && cd ~/docker-php
```
#### 构建镜像
```shell
# php
docker rmi fidding-php
docker build -t fidding-php php/.
```

#### 启动compose
```shell
docker-compose up -d
```

#### demo演示
1. 复制配置文件
    ```shell
    cp demo/demo.conf ~/docker-data/nginx/conf.d && cp -rf demo/www/demo ~/docker-data/www
    ```
2. 重启
    ```shell
    docker-compose restart
    ```
3. 配置本地host
    ```shell
    127.0.0.1   docker-php-demo.com
    ```
4. 打开浏览器访问地址

    [docker-php-demo.com](http://docker-php-demo.com)
    
   
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
