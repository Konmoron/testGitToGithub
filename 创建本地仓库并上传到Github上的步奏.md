# �������زֿⲢ�ϴ���Github��

1. �ڵ�ǰĿ¼����һ����Ҫ�ϴ����ļ��У�Ҳ���ֿ⣺
```
$ mkdir testGitToGithub
```
2. ���ļ��в���ʼ��
```
cd testGitToGithub
git init
```
��ʱ�����ļ����������һ�����ص�`.git`�ļ���
3. ����Github����ֿ�  
```
git remote add origin https://github.com/Konmoron/testGitToGithub.git
```
4. pull Github�ϵĲֿ�
```
git pull origin master --allow-unrelated-histories
```
5. �������ļ���ӵ��ֿ�
```
git add .
```
6. �ύ�ļ�  
```
git commit -m "Commit_Message"
``` 
7. �ϴ����زֿ�
```
git push -u origin master
```