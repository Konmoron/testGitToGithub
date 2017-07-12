# Git学习总结
----

**Git**是分布式控制系统，用于版本控制。

## 设置用户名和邮箱
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

## 查看用户名和邮箱

```
git config user.name
git config user.email
```

## 下载Github上的代码库

```
git clone [url=代码库的地址]
```
下载到当前目录。

如果需要保持代码的同步，需要**切换到下载的目录里面，使用如下代码：**
```
git remote add upstream [url=代码库的地址]
```

## 创建本地仓库并上传到Github上

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



