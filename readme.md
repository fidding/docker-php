
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