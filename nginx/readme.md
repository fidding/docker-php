
### 基本介绍
1. nginx: 1.17.5
2. 端口: 80
3. 配置目录: ~/conf.d
4. 项目目录: ~/www

### 后台启动
```shell
docker run --name fidding-nginx -d -p 80:80 -v $HOME/www:/www -v $HOME/conf.d:/etc/nginx/conf.d --link php-fpm:php-fpm nginx
```

### 查看日志
```shell
docker logs fidding-nginx
```
#### 重启/启动/停止
docker restart/start/stop fidding-nginx


