# tag的使用
****
## 新增文件*test-tag.txt*
初始内容为：
> This is a file to test tag!
> There is a bug in this!!!!!!!!!!!!!!!
> write other program!

## 添加并提交
```
git add test-tag.txt
git commit test-tag.txt -m "add test-tag.txt"
git push origin dev
```
## 回到`master`，增加一个tag:`v1.0`
```
git checkout master
git merge dev
git tag v1.0
```
## 推送到远程
```
git push origin master
git push origin v1.0 // 推送v1.0
```
## 进入`dev`分支编码
打开*test-tag.txt*，在文件末尾写入：
> wirte something!

此时发现`v1.0`有个bug。先提交`dev`里面的修改。
```
git add test-tag.txt
git commit test-tag.txt -m "change test-tag.txt"
```
## 根据`v1.0`，创建bugfix分支
`git checkout -b bugfix v1.0`
## 修改*test-tag.txt*里面的bug
> Fix this bug in this //There is a bug in this!!!!!!!!!!!!!!!

## 添加并提交
```
git add test-tag.txt
git commit test-tag.txt -m "fix bug in test-tag.txt
```
## 回到`master`分支，合并提交
```
git checkout master
git merge bugfix
git push origin master
git tag v2.0
git push origin v2.0
```
## 回到`dev`分支，合并`master`
```
git checkout dev
git merge master
```
此时会有冲突，合并的文件为：

> This is a file to test tag!
> Fix this bug in this //There is a bug in this!!!!!!!!!!!!!!!
> write other program!
> <<<<<<< HEAD
> write something!
> =======
> >>>>>>> master

修改冲突，将修改bug后的代码添加到test-tag.txt里面，修改后的文件为：

> This is a file to test tag!
> Fix this bug in this //There is a bug in this!!!!!!!!!!!!!!!
> write other program!
> write something!

## 添加并提交
```
git add test-tag.txt
git commit -m "fix conflict in test-tag.txt"
```
修改完成，bug修复完毕，即可继续编写其他代码。
