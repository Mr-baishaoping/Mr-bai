#今天学习了git上传文件

##下面是操作流程：

1.连接github

 ssh-keygen -t rsa -C "注册的github的邮箱"
 ssh-keygen -t rsa -C "liujunhang2018@163.com"
	一路回车就好

 打开用户主目录：C:\Users\用户名\.ssh
	里面存在两个文件：id_rsa  id_rsa.pub

 打开github -> settings -> SSH and GPG keys -> New SSH key -> title任意填写 、key里面填id_rsa.pub
 的内容
2. 第一次提交数据
    找到需要上传文件的目录，执行
     git init
     输入下面的命令进行配置
     git config --global user.email "you@example.com"
     git config --global user.name "Your Name"

 然后执行下面的命令
 git add *  将当前目录的所有文件全部添加到临时区
 git commit -m "提交声明"    将数据添加到本地仓库
 git remote add origin https://github.com/liujunhang2018/gittest.git  连接设置的仓库
 git push -u origin master 将本地数据提交到远程仓库