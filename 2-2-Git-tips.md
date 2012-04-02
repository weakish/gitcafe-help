# Git Tips

### 1.删除远程服务器上的某个分支

	git push origin :branchname 


### 2.Fork 项目与上游代码库保持同步：

* 在 Fork 的代码库中添加上游代码库的 remote 源，（操作一次就可以，以后不必每次添加）

		git remote add upstream git://gitcafe.com/username/upstream 
		#upstream 表示上游代码库名称
	
* 本地修改和提交 (commit)

* 在每次 Pull Request 前做如下操作，即可实现和上游版本库的同步。
	
		git remote update upstream
		git rebase upstream/master  
		# 如果不是 master 分支，请把 master 改为相应的分支名，
		同时在 rebase 前用 git checkout 命令切换到相应的本地分支	

* Push 代码到 GitCafe

		git push
	
	[参考]：[ProGit-分支的衍合](http://progit.org/book/zh/ch3-6.html)

### 3.

