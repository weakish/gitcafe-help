# 安装和设置 Git

GitCafe 是以 Git 

### 1.下载及安装 Git  

根据你当前使用的系统平台，请到 [Git 官方网站][Git]下载相应的客户端软件。

[Mac OSX][Mac]  / [Windows][Win] / [Linux][Linux] / [Solaris][Solaris]

[Git]:http://git-scm.com/download/
[Mac]:http://git-scm.com/download/mac
[Win]:http://git-scm.com/download/win
[Linux]:http://git-scm.com/download/linux
[Solaris]:http://git-scm.com/download/linux

'如果你对 Git 完全不熟悉，建议你先阅读 《[Pro Git 中文版](http://progit.org/book/zh/)》一书'

### 2.创建 SSH 秘钥

在你的电脑与 GitCafe 服务器之间保持通信时，我们使用 SSH key 认证方式来保证通信安全。所以在使用 GitCafe 前你必须先建创自已的 SSH key。

1). 

### 3.添加 SSH 公钥到 GitCafe

1). 用文本工具打开 `~/.ssh/id_rsa.pub` 文档，复制里面的所有内容到剪贴板。

2). 进入 GitCafe -->[账户设置][3-1]-->[SSH 公钥管理][3-2]设置项，点击[添加新公钥][3-3] 按钮，在 Title 文本框中输入任意字符，在 Key 文本框粘贴刚才复制的公钥字符串，按保存按钮完成操作。

[3-1]:http://gitcafe.com/account
[3-2]:http://gitcafe.com/account/public_keys
[3-3]:http://gitcafe.com/account/public_keys/new

### 4.测试连接

以上步骤完成后，你就可以通过以下命令来测试是否可以连接 GitCafe 服务器了。

`ssh -T git@gitcafe.com`

如果是第一次连接的话，会出现以下警告，不用担心，输入 yes 按回车就可以了。

>The authenticity of host 'gitcafe.com (50.116.2.223)' can't be established.
>#RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
>#Are you sure you want to continue connecting (yes/no)?

最后，如果连接成功的话，会出现以下信息。

>Hi username! You've successfully authenticated, but GitCafe does not provide shell a
ccess.

### 5.完成

测试通过后，你就可以到 GitCafe 上创建 Git 项目并上传代码了。