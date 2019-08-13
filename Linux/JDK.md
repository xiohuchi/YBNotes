# CentOS安装JDK

### 1.卸载

查看已经安装的jdk

```
[root@www /]# rpm -qa|grep jdk
copy-jdk-configs-3.3-10.el7_5.noarch
java-1.8.0-openjdk-1.8.0.181-7.b13.el7.x86_64
java-1.8.0-openjdk-headless-1.8.0.181-7.b13.el7.x86_64
```

卸载命令

```
[root@www /]# yum -y remove java-1.8.0-openjdk-headless-1.8.0.181-7.b13.el7.x86_64
```

卸载完成之后Java命令不被识别

```
[root@www /]# java -version 
bash: java: command not found...
```

### 2.安装

去官网下载jdk：http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html

解压到安装目录

```
[root@www /jdk]# tar -zxvf jdk-8u221-linux-x64.tar.gz -C /data/jdk/
```

安装完毕之后在/etc/profile文件末尾添加

```
[root@www /jdk]# vim /etc/profile
export JAVA_HOME=/data/jdk/jdk1.8.0_221
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH
```

使/etc/profile生效

```
[root@www /jdk]# source /etc/profile
```

检测安装是否成功

```
[root@www /jdk]# java -version
```

