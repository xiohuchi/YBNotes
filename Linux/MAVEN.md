## 安装Maven

Maven的下载地址是：http://maven.apache.org/download.cgi

### 1.下载的压缩文件解压

```
wget http://mirror.bit.edu.cn/apache/maven/maven-3/3.6.1/binaries/apache-maven-3.6.1-bin.tar.gz
tar vxf apache-maven-3.6.1-bin.tar.gz
mv apache-maven-3.6.1 /data/maven/apache-maven-3.6.1
```

### 2.修改环境变量

 在/etc/profile中添加以下几行

```
[root@www /jdk]# vim /etc/profile

export MAVEN_HOME=/data/maven/apache-maven-3.6.1
export MAVEN_HOME export PATH=${PATH}:${MAVEN_HOME}/bin
```

使/etc/profile生效

```
[root@www /jdk]# source /etc/profile
```

检测安装是否成功

```
[root@www /jdk]# mvn -version
```



西西的配置

MAVEN_HOME=/usr/local/java/apache-maven-3.6.1 export MAVEN_HOME export PATH=${PATH}:${MAVEN_HOME}/bin