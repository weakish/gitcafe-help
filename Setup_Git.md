# 安装和设置 Git

GitCafe 是以版本控制软件 [Git][Git] 为核心的网络服务，所以在使用 GitCafe 服务之前，你必须了解及掌握如何使用 Git 工具。通过以下步骤你就可以学会如何安装和设置 Git 软件，并能顺利连接 GitCafe 服务器。

>如果你对 Git 完全不熟悉，想全面学习 Git 知识的话，建议阅读 《[Pro Git 中文版](http://progit.org/book/zh/)》一书。

### 1.下载及安装 Git  

根据你当前使用的系统平台，请到 [Git 官方网站][GitDownload]下载相应的客户端软件。

快速下载链接： [Mac OSX][Mac]  / [Windows][Win] / [Linux][Linux]

下载并安装完成后，通常在 Mac OSX 及 Linux 平台下我们用**终端工具 (Terminal)** 来使用 Git ，而在 Windows 平台下用 **Git Bash** 工具。

![Git Bash 工具](http://gitcafe.com/GitCafe/Help/raw/master/Images/git_bash.png)

[Git]:http://git-scm.com
[GitDownload]:http://git-scm.com/download/
[Mac]:http://git-scm.com/download/mac
[Win]:http://git-scm.com/download/win
[Linux]:http://git-scm.com/download/linux


### 2.创建 SSH 秘钥

在你的电脑与 GitCafe 服务器之间保持通信时，我们使用 SSH key 认证方式来保证通信安全，所以在使用 GitCafe 前你必须先建创自已的 SSH key。

1). 进入 SSH 目录

`cd ~/.ssh`

2). 生成新的 SSH 秘钥 (记得把以下命令中的 `your_email@youremail.com` 改为你的 Email 地址 )

`ssh-keygen -t rsa -C "your_email@youremail.com"`

3). 生成过程中会出现以下信息，按屏幕提示操作，并记得输入 passphrase

    $ ssh-keygen -t rsa -C "your_email@youremail.com"
    Generating public/private rsa key pair.
    Enter file in which to save the key (/c/Users/username/.ssh/id_rsa):
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    Your identification has been saved in /c/Users/username/.ssh/id_rsa.
    Your public key has been saved in /c/Users/username/.ssh/id_rsa.pub.
    The key fingerprint is:
    15:81:d2:7a:c6:6c:0f:ec:b0:b6:d4:18:b8:d1:41:48 your_email@youremail.com

4). SSH 秘钥生成结束后，你可以在用户目录 (~/.ssh/) 下看到私钥 `id_rsa` 和公钥 `id_rsa.pub` 这两个文件，记住千万不要把私钥文件 `id_rsa` 透露给任何人。

### 3.添加 SSH 公钥到 GitCafe

1). 用文本工具打开公钥文件 `~/.ssh/id_rsa.pub` ，复制里面的所有内容到剪贴板。

2). 进入 GitCafe -->[账户设置][3-1]-->[SSH 公钥管理][3-2]设置项，点击[添加新公钥][3-3] 按钮，在 Title 文本框中输入任意字符，在 Key 文本框粘贴刚才复制的公钥字符串，按保存按钮完成操作。

![添加公钥](http://gitcafe.com/GitCafe/Help/raw/master/Images/add_ssh_key.png)

[3-1]:http://gitcafe.com/account
[3-2]:http://gitcafe.com/account/public_keys
[3-3]:http://gitcafe.com/account/public_keys/new

### 4.测试连接

以上步骤完成后，你就可以通过以下命令来测试是否可以连接 GitCafe 服务器了。

`ssh -T git@gitcafe.com`

如果是第一次连接的话，会出现以下警告，不用担心，输入 yes 按回车就可以了。

    The authenticity of host 'gitcafe.com (50.116.2.223)' can't be established.
    #RSA key fingerprint is 84:9e:c9:8e:7f:36:28:08:7e:13:bf:43:12:74:11:4e.
    #Are you sure you want to continue connecting (yes/no)?

最后，如果连接成功的话，会出现以下信息。

    Hi username! You've successfully authenticated, but GitCafe does not provide shell access.

### 5.完成

测试通过后，你就可以到 GitCafe 上[创建 Git 项目][New_Project]并上传代码了。

[New_Project]:http://gitcafe.com/projects/new