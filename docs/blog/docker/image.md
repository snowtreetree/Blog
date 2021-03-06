# 镜像

当运行容器（container）时，如果是用的镜像不存在，Docker会自动从Docker镜像仓库上下载。

## 镜像使用

### 镜像列表

```bash
$ docker images
REPOSITORY                TAG                 IMAGE ID            CREATED             SIZE
test/ubuntu               v1                  407773070e04        42 hours ago        73.9MB
new_test_ubuntu           latest              656b0a7ca0ae        42 hours ago        73.9MB
arestest                  latest              9dc37dfffd30        3 days ago          926MB

# REPOSITORY 镜像仓库源
# TAG 镜像tag，同一个镜像可以有多个tag
# IMAGE ID 镜像ID
# CREATED 创建时间
# SIZE 镜像大小
```

#### 运行容器

```bash
$ docker run -it -p 7070:8080 ububtu:15.10 /bin/bash
# ububtu:15.10 置顶镜像版本运行容器
# p 设置端口 7070 代表主机端口，8080代表容器端口
# P 随机端口

```

#### 查找/删除容器

```bash
# 查找
$ docker search httpd
# 删除
$ docker rmi httpd
```


#### 数据卷

主机和容器数据共享

```bash
$ docker run -it -v /test:/test 7070:8080 centos
```

