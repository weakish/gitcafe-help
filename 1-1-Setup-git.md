[返回目录](README.md#code)

# 安装和设置 Git

### 1.下载及安装 Git  

* Windows 用户：到这里下载最新版本 [Git for Windows](http://code.google.com/p/msysgit/downloads/list)，并全都按照默认选项进行安装。安装完后我们通常使用 Git Bash 工具就可以了。

* Linux 用户: Ubuntu 及 Fedora 等 Linux 用户可直接通过操作系统的包管理软件来安装 Git 。

	Ubuntu/Debian 在终端下输入如下命令:

		$ sudo apt-get install git-core

	Fedora/RedHat/CentOS 在终端下输入如下命令:

		$ yum install git-core

* Mac 用户： 到这里下载并安装最新版本的 [Git for Mac OSX](http://code.google.com/p/git-osx-installer/downloads/list?can=3)。
		

### 2.生成及上传 SSH key

在你的电脑与 GitCafe 服务器之间保持通信时，我们使用 SSH key 认证方式来保证通信安全。
所以在使用 GitCafe 前你必须先建创自已的 SSH key。

1. 检查是否已存在 ssh key 

		$ cd ~/.ssh
	
	如果该目录存在，那么就表示之前已生成过 SSH key。

* 备份旧的 SSH key

[返回目录](README.md#code)

	
