## git 命令

* git init 

* git clone

============================

* git add 文件名
* git add .
* git commit -m "备注"
* git reset --hard HEAD
* git checkout -- 文件名
* git remote add origin [ssh地址]  
* git push -u origin master
* git push
* git remote add origin [ssh地址] 

=============================

* git status 
* git log 
* git log --pretty=oneline
* git log --graph  --pretty=oneline --abbrev-commit
* git reflog
* git rm
* git diff 

=============================

* git checkout -b 分支名 `创建+切换分支`
* git branch 分支名 `创建分支`
* git checkout 分支名 `切换分支`
* git branch `查看当前分支，列出所有分支，当前分支前面会标一个\*号。`
* git merge `合并某分支到当前分支`
* git branch -d 分支名 `删除分支`
* git branch -D 分支名 `强行删除分支`



=============================

_Fast forward_· `快速合并,，但这种模式下，删除分支后，会丢掉分支信息` 

_--no-ff_  `禁用Fast forward模式,如果要强制禁用Fast forward模式，Git就会在merge时生成一个新的commit，这样，从分支历史上就可以看出分支信息。`

```javascript
	git merge --no-ff -m "merge with no-ff" dev
```
* git log --graph `可以看到分支合并图`


* git stash  `可以把当前工作存储起来，等以后恢复现场继续工作`
* git stash list `查看存储的工作`
* git stash apply `恢复存储的工作，但不删除stash内容`
* git stash drop `删除stash内容`
* git stash pop `恢复存储的工作，也删除stash内容`



* git remote `查看远程库的信息`
* git remote -v  `查看远程库的详情信息 ` 

* 如果git pull提示 `notacking information`
* git branch --set-upsteam-to `分支名` origin `分支名`  `创建本地分支和远程分支的链接关系`
* 

* git checkout -b `分支名` origin/`分支名`  `在本地创建和远程分支对应的分支，本地和远程分支的名称最好一致`




> rebase 

* git rebase `变基`
> rebase 操作可以把本地未push分叉提交历史整理成直线；
> rebase 的目的是使我们在查看历史提交的变化是更容易，因为分叉的提交需要三方对比
	
> tag 

* git tag `<标签名字>` `创建单个标签，默认HEAD,也可以提供一个commit ID ` 
* git tag `<commit ID>`     
* git tag `可以查看所有标签`
* git show `<tagName>` `查看<tagName>标签的信息` 
* git  tag -a `<标签名字>` -m `<便签描述>`  `commit ID`   `<-a> 指定标签名字，<-m> 说明文字`

> 删除便签 
<small>创建的标签都只存储在本地，不会自动推送到远程。所以，打错的标签可以在本地安全删除。<small>


* git push origin <tagname>  `可以推送一个本地标签；`

* git push origin --tags `可以推送全部未推送过的本地标签；`

* git tag -d <tagname> `可以删除一个本地标签；`

* git push origin :refs/tags/<tagname> `可以删除一个远程标签。`