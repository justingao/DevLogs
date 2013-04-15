在 GitHub 上创建项目的过程
========================================================================

1.  在 GitHub 网站上手动创建一个项目。
2.  下载并安装 Git 客户端工具。
3.  设置 git 客户端（Windows 上是打开 Git Bash 工具进入命令行模式）：    
    ```
    git config --global user.name "MyUserName" 
    git config --global user.email "MyE-mail" 
    ```
4.  克隆服务器上的代码到本地：   
    ```
    git clone https://github.com/justingao/DevLogs.git
    ```
5.  修改本地文件之后，提交：    
    ```
    git commit -m "CommitMessages"
    ```
6.  同步本地代码到服务器上：    
    ```
    git remote add origin git@github.com:MyUserName/DevLogs.git 
    git push -u origin master
    ```


使用 SSH 密钥访问 GitHub
========================================================================
1.  生成本地的 SSH 公钥与私钥：    
    ```
    ssh-keygen -t rsa -C "MyE-mail"
    ```
2.  将公钥添加到 GitHub 服务器上。
3.  添加完成之后，使用下面的命令测试能否免密码访问 GitHub 网站：    
```
ssh -T git@github.com
```    
如果信任关系创建正常的话，界面上会有提示：    
```
Hi MyUserName! You've successfully authenticated, but GitHub does not provide shell access.
```

这个页面有详细的指导：<https://help.github.com/articles/generating-ssh-keys>

测试过程中发现即使做了如上设置，但是执行 `git push origin master` 的时候，还是会提示输入用户名和密码。后经检查，是由于提交方式是 https 方式，而不是 ssh 方式。检查方法：    
```
git remote -v
```
修改方式：    
```
git remote remove origin
git remote add origin git@github.com:MyUserName/DevLogs.git
```


