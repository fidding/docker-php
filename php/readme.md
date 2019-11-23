
### 基本介绍
1. php: 7.3
2. 端口: 9000
4. 项目目录: ~/www

### 构建镜像
```shell
docker build -t fidding/php-fpm .
```

### 后台启动
```shell
docker run -it -d --name php-fpm -p 9000:9000 -v $HOME/www:/www  --link fidding-mysql:mysql fidding/php-fpm
```