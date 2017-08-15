# play800
play800--OA的BUG

## git 简单教程：

### 1、初始化仓库
```javascript
git init   
```      

### 2、添加所有内容到预备提交里
```javascript
git add .   
```     

### 3、检查状态
```javascript
git status      
``` 


如果修改内容：
### 3.1、看下文件到底改了什么内容
```javascript
git diff 文件 (如：git diff readme.txt)   
```    


### 4、告诉Git，把文件提交到仓库
```javascript
git commit -u '丢雷老鼠--->提交注释'  
```           

### 5、配置好公钥，放在github的SSH Key上面的是公钥
```javascript
ssh-keygen  -t rsa –C 'youremail@example.com'  
```

### 6、把本地仓库的内容推送到GitHub仓库
```javascript
git remote add origin https://github.com/231716573/test.git
```

### 7、把本地master分支的最新修改推送到github上
```javascript
git push origin master
```


## 常见问题：

### 1、error: failed to push some refs to 'https://github.com/231716573/test.git'

出现错误的主要原因是github中的README.md文件不在本地代码目录中

可以通过如下命令进行代码合并【注：pull=fetch+merge]
```javascript
git pull --rebase origin master
```

此时再执行语句 git push -u origin master即可完成代码上传到github

### 2、