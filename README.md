使用下面命令下载自动重装系统脚本

wget --no-check-certificate -qO InstallNET.sh 'https://moeclub.org/attachment/LinuxShell/InstallNET.sh' && chmod a+x InstallNET.sh

系统重装命令:

在下面选择将要按的的系统，运行对应命令即可，一般20-30分钟就会安装完成。装默认root密码：Vicer。

安装CentOS 6.8 x32：

bash InstallNET.sh -c 6.8 -v 32 -a

安装CentOS 6.8 x64：

bash InstallNET.sh -c 6.8 -v 64 -a

安装CentOS 6.9 x32：

bash InstallNET.sh -c 6.9 -v 32 -a

安装CentOS 6.9 x64：

bash InstallNET.sh -c 6.9 -v 64 -a

安装Debian 7 x32：

bash InstallNET.sh -d 7 -v 32 -a

安装Debian 8 x64：

bash InstallNET.sh -d 8 -v 64 -a

安装Debian 9 x64：

bash InstallNET.sh -d 9 -v 64 -a

安装Ubuntu 14.04 x64：

bash InstallNET.sh -u trusty -v 64 -a

安装Ubuntu 16.04 x64：

bash InstallNET.sh -u xenial -v 64 -a

安装Ubuntu 18.04 x64：

bash InstallNET.sh -u bionic -v 64 -a
