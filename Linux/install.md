# 安装 CentOS 7
## 一、CentOS 7官方下载

CentOS 7官方下载地址：https://www.centos.org/download/

 在CentOS官方网站上，CentOS 7提供了三种ISO镜像文件的下载：DVD ISO、Everything ISO、Minimal ISO。
以下针对各个版本的ISO镜像文件，进行一一说明：

- CentOS-7.0-x86_64-DVD-1503-01.iso              标准安装版，一般下载这个就可以了（推荐）
- CentOS-7.0-x86_64-NetInstall-1503-01.iso       网络安装镜像（从网络安装或者救援系统）
- CentOS-7.0-x86_64-Everything-1503-01.iso     对完整版安装盘的软件进行补充，集成所有软件。（包含centos7的一套完整的软件包，可以用来安装系统或者填充本地镜像）
- CentOS-7.0-x86_64-GnomeLive-1503-01.iso   GNOME桌面版
- CentOS-7.0-x86_64-KdeLive-1503-01.iso         KDE桌面版
- CentOS-7.0-x86_64-livecd-1503-01.iso            光盘上运行的系统，类拟于winpe 
- CentOS-7.0-x86_64-minimal-1503-01.iso         精简版，自带的软件最少

## 二、安装

### 1.打开VMwear选择新建虚拟机

![1565599454589](C:\project\github\YBNotes\Linux\images\1565599454589.png)

### 2.典型安装与自定义安装

典型安装：VMwear会将主流的配置应用在虚拟机的操作系统上，对于新手来很友好。

自定义安装：自定义安装可以针对性的把一些资源加强，把不需要的资源移除。避免资源的浪费。

这里我选择自定义安装。

![1565599555563](C:\project\github\YBNotes\Linux\images\1565599555563.png)



### 3.虚拟机兼容性选择

这里要注意兼容性，因为不同版本的VMware对虚拟硬件支持情况不同。举个例子，老版本的只支持4G内存，新版本支持8G内存等等（本例子只是为了说明虚拟硬件的含义，不代表实际情况。）。因此如果需要改虚拟机运行在旧版本的VMware中，这里需要选择旧版本的VMware的版本号。这里我并不需要以后让该虚拟机运行在其他版本的VMware中，因此选择的就是默认的版本号，即正在使用的VMware版本号。在右下方的限制中，可以看到支持的虚拟硬件状况。选择好后，点击下一步。

![1565599684646](C:\project\github\YBNotes\Linux\images\1565599684646.png)

### 4.选择稍后安装操作系统

接下来根据实际情况选择要安装的操作系统。本文这里选择Linux系统，版本号为CentOS 7 64位，之后点击下一步。

![1565599816056](C:\project\github\YBNotes\Linux\images\1565599816056.png)


