# git教程

## 重点参考的git教程：
```javascript
http://blog.csdn.net/free_wind22/article/details/50967723
``` 

## git 简单教程：

#### 1、初始化仓库
```javascript
git init   
```      

#### 2、添加所有内容到预备提交里
```javascript
git add .   
```     

#### 3、检查状态
```javascript
git status      
``` 


如果修改内容：
#### 3.1、看下文件到底改了什么内容
```javascript
git diff 文件 (如：git diff readme.txt)   
```    


#### 4、告诉Git，把文件提交到仓库
```javascript
git commit -m '丢雷老鼠--->提交注释'  
```           

#### 5、配置好公钥，放在github的SSH Key上面的是公钥
```javascript
ssh-keygen  -t rsa –C 'youremail@example.com'  
```

#### 6、把本地仓库的内容推送到GitHub仓库
```javascript
git remote add origin https://github.com/231716573/test.git
```

#### 7、把本地master分支的最新修改推送到github上
```javascript
git push origin master
```

### git 后续修改：

```javascript
git add .  
```

```javascript
git commit -m '此处自己编写注释'  
```

```javascript
git push -u origin master
```


## 常见问题：(后续陆续补上)

#### 1、error: failed to push some refs to 'https://github.com/231716573/test.git'

出现错误的主要原因是github中的README.md文件不在本地代码目录中

可以通过如下命令进行代码合并【注：pull=fetch+merge]
```javascript
git pull --rebase origin master
```

此时再执行语句 git push -u origin master即可完成代码上传到github

#### 2、git add

git add . 是全部文件，如果想单独上传指定文件，可以例如： git add text.txt 或者 git add haha.html

#### 3、git remote只需要提交一次

```javascript
$ git remote add origin https://github.com/231716573/play800.git
fatal: remote origin already exists.
```
代表此处可以省略，直接git push origin master即可。


#### 4、pathspec '' did not match any file(s) know to git.
```
使用：git commit -m '注释'，不要使用：git commit -u '注释'
```
