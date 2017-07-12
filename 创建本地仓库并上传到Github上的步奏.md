# 创建本地仓库并上传到Github上

1. 在当前目录创建一个需要上传的文件夹，也即仓库：
```
$ mkdir testGitToGithub
```
2. 打开文件夹并初始化
```
cd testGitToGithub
git init
```
此时，该文件夹下面会有一个隐藏的`.git`文件夹
3. 关联Github代码仓库  
```
git remote add origin https://github.com/Konmoron/testGitToGithub.git
```
4. pull Github上的仓库
```
git pull origin master --allow-unrelated-histories
```
5. 将所有文件添加到仓库
```
git add .
```
6. 提交文件  
```
git commit -m "Commit_Message"
``` 
7. 上传本地仓库
```
git push -u origin master
```