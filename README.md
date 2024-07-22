# Redis Docker Compose YML File


## 简介
    docker 一键启动 redis 容器的 docker-compose.yml 配置


## 镜像环境：
	redis:7.2.5


## 导入镜像：
	docker load -i 镜像包


## 启动命令：
	docker-compose up -d


##  安装及生成数据路径：
    ├── redis 
        ├── images                      镜像文件文件目录
        ├── redis                       容器挂载目录
            ├── conf                        配置文件目录
                └── redis.conf                 redis 配置文件
            ├── data                        数据目录
            ├── log                         日志目录
        ├── docker-compose.yml          docker-compose.yml
        └── README.md                   README.md


## 隐私信息配置：
### 1. 修改密码, 文件路径：./redis/conf/redis.conf
    # 默认打开，限制redis只能本地访问。注释掉
    # bind 127.0.0.1  
    # 默认yes，开启保护模式，限制为本地访问
    protected-mode no 
    # 密码
    requirepass xxx


## 后续操作：
### 1. 设置日志目录：./redis/conf/redis.conf 
    logfile "/var/log/redis/redis-server.log"


