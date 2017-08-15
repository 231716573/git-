# play800
play800--OA的BUG

# git 简单教程：

1、初始化仓库
git init         

2、添加所有内容到预备提交里
git add .        

3、检查状态
git status       


如果修改内容：
3.1、看下文件到底改了什么内容
git diff 文件 (如：git diff readme.txt)       


4、告诉Git，把文件提交到仓库
git commit -u '丢雷老鼠--->提交注释'             

5、配置好公钥，放在github的SSH Key上面的是公钥
ssh-keygen  -t rsa –C 'youremail@example.com'  

6、把本地仓库的内容推送到GitHub仓库
git remote add origin https://github.com/231716573/test.git

7、把本地master分支的最新修改推送到github上
git push origin master


