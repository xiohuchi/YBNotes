#### 安装docker

#### 1）安装依赖包

```
yum install -y yum-utils device-mapper-persistent-data lvm2
```

#### 2）添加Docker软件包源：

```
yum-config-manager \
--add-repo \
https://download.docker.com/linux/centos/docker-ce.repo
```

#### 3）安装Docker CE

```
 yum install docker-ce -y
```

#### 4）配置加速器(没用上)

```
curl -sSL https://get.daocloud.io/daotools/set_mirror.sh | sh -s http://bc437cce.m.daocloud.io`
 #因为默认源会去国外获取数据，所以会慢可以超时，这是我们就需要配置加速器指向国内源https://www.daocloud.io/
```

#### 5）启动并开机启动

```
$  systemctl start docker
$  systemctl enable docker
```

#### 6）建立 docker 用户组

```
$  groupadd docker
$  usermod -aG docker $USER
```

#### 7）测试 Docker 是否安装正确

```
docker run hello-world
```

#### 8）查看docker版本

```
$  docker version
```

