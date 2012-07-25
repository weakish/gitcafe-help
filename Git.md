# Git 入门

## 什么是 Git?

Git 是由 Linux 之父 Linus Tovalds 为了更好地管理linux内核开发而创立的分布式版本控制／软件配置管理软件。目前支持 Windows 、MacOSX 、Linux 等多种主流平台，特点为快速、高效及易于使用。

* [Git 官方网站](http://git-scm.com/)

## 新手入门教程推荐

* Pro Git [(中文版)](http://progit.org/book/zh/) / [(英文版)](http://progit.org/)

* Git Community Book [(中文版)](http://gitbook.liuhui998.com/index.html) / [(英文版)](http://book.git-scm.com/)

# Git Tips

### 1.删除远程服务器上的某个分支

`git push origin :branchname` 


### 2.Fork 项目与上游代码库保持同步：

* 在 Fork 的代码库中添加上游代码库的 remote 源，（操作一次就可以，以后不必每次添加）

    `git remote add upstream git://gitcafe.com/username/upstream` 
    
    #upstream 表示上游代码库名称
  
* 本地修改和提交 (commit)

* 在每次 Pull Request 前做如下操作，即可实现和上游版本库的同步。
  
    `git remote update upstream`
    `git rebase upstream/master`  
    
    #如果不是 master 分支，请把 master 改为相应的分支名，
    同时在 rebase 前用 git checkout 命令切换到相应的本地分支 

* Push 代码到 GitCafe

    `git push`
  
  [参考]：[ProGit-分支的衍合](http://progit.org/book/zh/ch3-6.html)