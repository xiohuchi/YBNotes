# CentOS7安装JDK1.8

### 1.卸载

查看已经安装的jdk

```
[root@bogon /]# rpm -qa|grep jdk
java-1.8.0-openjdk-headless-1.8.0.65-3.b17.el7.x86_64
java-1.7.0-openjdk-1.7.0.91-2.6.2.3.el7.x86_64
java-1.7.0-openjdk-headless-1.7.0.91-2.6.2.3.el7.x86_64
java-1.8.0-openjdk-1.8.0.65-3.b17.el7.x86_64
```

卸载命令

```
[root@bogon /]# yum -y remove java-1.8.0-openjdk-headless-1.8.0.65-3.b17.el7.x86_64
```

**卸载**

查看已经安装的jdk

[root@bogon jre]# rpm -qa|grep jdk java-1.8.0-openjdk-headless-1.8.0.65-3.b17.el7.x86_64 java-1.7.0-openjdk-1.7.0.91-2.6.2.3.el7.x86_64 java-1.7.0-openjdk-headless-1.7.0.91-2.6.2.3.el7.x86_64 java-1.8.0-openjdk-1.8.0.65-3.b17.el7.x86_64

卸载命令

[root@bogon jre]# yum -y remove java-1.8.0-openjdk-headless-1.8.0.65-3.b17.el7.x86_64



卸载完成之后Java命令不被识别

[root@bogon lib]# java -version bash: java: command not found...



**安装**

去官网下载jdk：http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html 

解压到安装目录

[root@bogon software]# tar -zxvf jdk-8u211-linux-x64.tar.gz -C /usr/local/java/



安装完毕之后在/etc/profile文件末尾添加

[root@bogon software]# vim /etc/profile export JAVA_HOME=/usr/local/java/jdk1.8.0_181 export JRE_HOME=${JAVA_HOME}/jre export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib export PATH=${JAVA_HOME}/bin:$PATH

使/etc/profile生效

[root@bogon jdk1.8.0_101]# source /etc/profile



检测安装是否成功

[root@bogon jdk1.8.0_101]# java -version