# 萌咖大佬的一键DD脚本
一键网络重装纯净版Debian/Ubuntu/CentOS系统脚本是由萌咖博主制作的，可以为的Linux系统VPS简单快速的一键网络重装Debian、Ubuntu、CentOS纯净版系统，目前此脚本不支持OpenVZ架构的VPS，全自动安后装默认root密码：MoeClub.org，安装完成后请自行更改密码。

### 背景:

适用于由GRUB引导的CentOS,Ubuntu,Debian系统.

使用官方发行版去掉模板预装的软件.

同时也可以解决内核版本与软件不兼容的问题。

只要有root权限,还您一个纯净的系统。

注意:

全自动安装默认root密码:```  MoeClub.org  ```指定密码参数后面加 ```-p 密码```

使用默认密码安装完成后请立即更改密码.

能够全自动重装Debian/Ubuntu/CentOS等系统.

全自动安装CentOS时默认提供VNC功能,可使用VNC Viewer查看进度,VNC端口为1或者5901,可自行尝试连接.(成功后VNC功能会消失.),目前CentOS只支持重装为CentOS6。

特别注意:OpenVZ构架不适用.

确保安装了所需软件:

#### Debian/Ubuntu:
```
apt-get install -y xz-utils openssl gawk file
```
#### RedHat/CentOS:
```
yum install -y xz openssl gawk file
```
如果出现了错误,请运行:

#### Debian/Ubuntu:
```
apt-get update
```
#### RedHat/CentOS:
```
yum update
```
```
Usage:
        bash InstallNET.sh      -d/--debian [dist-name]
                                -u/--ubuntu [dist-name]
                                -c/--centos [dist-version]
                                -v/--ver [32/i386|64/amd64]
                                --ip-addr/--ip-gate/--ip-mask
                                -apt/-yum/--mirror
                                -dd/--image
                                -a/-m
 
# dist-name: 发行版本代号
# dist-version: 发行版本号
# -apt/-yum/--mirror : 使用定义镜像
# -a/-m : 询问是否能进入VNC自行操作. -a 为不提示(一般用于全自动安装), -m 为提示.
# --ip-addr :IP Address/IP地址
# --ip-gate :Gateway   /网关
# --ip-mask :Netmask   /子网掩码
# 以下示例中,将X.X.X.X替换为自己的网络参数.
```

# 快速使用示例:

### 自动下载重装命令:
```
wget --no-check-certificate -qO NetReInstall.sh 'https://raw.githubusercontent.com/huxuansong/NetReInstall/main/NetReInstall.sh' && chmod a+x NetReInstall.sh
```
### 手动下载重装命令:

在下面选择将要按的的系统，运行对应命令即可，一般20-30分钟就会安装完成。装默认root密码：MoeClub.org。

### 安装CentOS 6.8 x32：

bash NetReInstall.sh -c 6.8 -v 32 -a

### 安装CentOS 6.8 x64：

bash NetReInstall.sh -c 6.8 -v 64 -a
```
bash NetReInstall.sh -c 6.8 -v 64 -a --mirror 'http://mirror.centos.org/centos'
```
### 安装CentOS 6.9 x32：

bash NetReInstall.sh -c 6.9 -v 32 -a

### 安装CentOS 6.9 x64：

bash NetReInstall.sh -c 6.9 -v 64 -a

### 安装Debian 7 x32：

bash NetReInstall.sh -d 7 -v 32 -a

### 安装Debian 8 x64：

bash NetReInstall.sh -d 8 -v 64 -a

### 安装Debian 9 x64：

bash NetReInstall.sh -d 9 -v 64 -a

### 安装Ubuntu 14.04 x64：

bash NetReInstall.sh -u trusty -v 64 -a

bash NetReInstall.sh -u 14.04 -v 64 -a

### 安装Ubuntu 16.04 x64：

bash NetReInstall.sh -u xenial -v 64 -a

bash NetReInstall.sh -u 16.04 -v 64 -a

### 安装Ubuntu 18.04 x64：

bash NetReInstall.sh -u bionic -v 64 -a

bash NetReInstall.sh -u 18.04 -v 64 -a

### 安装Ubuntu 20.04 x64：

bash NetReInstall.sh -u 20.04 -v 64 -a


###  甲骨文ARM:
```
bash <(wget --no-check-certificate -qO- 'https://git.io/JeiRm') -d 10 -v arm64 -a
```
### CentOS系统用萌咖dd脚本出现Not Found grub.的解决方法
```
grub2-mkconfig -o /boot/grub2/grub.cfg
```

### VPS或者独立服务器有多个网卡.
##### 例:安装debian9，网卡名称enp0s5和enp0s6,enp0s6可用.
```
bash <(wget --no-check-certificate -qO- 'https://git.io/JeiRm') -d 9 -v 64 -a -i enp0s6
```
### VPS安装debian9并且自定义源.
```
bash <(wget --no-check-certificate -qO- 'https://git.io/JeiRm') -d 9 -v 64 -a --mirror 'http://archive.debian.org/debian/'
```
### VPS安装debian9无法识别IP地址并且自定义源.
```
bash <(wget --no-check-certificate -qO- 'https://git.io/JeiRm') -d 9 -v 64 -a --ip-addr x.x.x.x --ip-gate x.x.x.x --ip-mask x.x.x.x  --mirror 'http://archive.debian.org/debian/'
```
### VPS安装debian8并且自定义源.
```
bash NetReInstall.sh -d 8 -v 64 -a --mirror 'http://archive.debian.org/debian'
```
### VPS安装Ubuntu 14.04 x64并且自定义源.
```
bash NetReInstall.sh -u 14.04 -v 64 -a --mirror 'http://archive.ubuntu.com/ubuntu'
```

## 一些可用镜像地址:
```
# 推荐使用带有 /GoogleDrive/<File_ID> 链接, 速度更快.
# 当然也可以使用自己GoogleDrive中储存的镜像,使用方式:
  https://image.moeclub.org/GoogleDrive/<File_ID>
 
# win7emb_x86.tar.gz:
  https://image.moeclub.org/GoogleDrive/1srhylymTjYS-Ky8uLw4R6LCWfAo1F3s7 
  https://image.moeclub.org/win7emb_x86.tar.gz
 
# win8.1emb_x64.tar.gz:
  https://image.moeclub.org/GoogleDrive/1cqVl2wSGx92UTdhOxU9pW3wJgmvZMT_J
  https://image.moeclub.org/win8.1emb_x64.tar.gz
```


