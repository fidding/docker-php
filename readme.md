
### 目录
```shell
.
├── docker-compose.yaml
├── mysql
│   ├── data sql数据目录
│   └── readme.md
├── nginx ng目录
│   ├── conf.d ng配置目录
│   ├── log ng日志目录
│   └── readme.md
├── php php目录
│   ├── conf.d php扩展配置目录
│   ├── Dockerfile
│   └── readme.md
├── readme.md
└── www 项目目录
```
### 构建镜像
```shell
# php
docker build -t fidding/php-fpm php/.
```

### 启动compose
```shell
docker-compose up -d
```

### compose操作 
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