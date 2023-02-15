# 远程仓库
###### 1.  创建SSH KEY
在用户主目录下创建.ssh目录
``
$ ssh-keygen -t rsa -C "youremail.com"
``
其中`id_rsa`是私匙，不能泄露出去；`id_rsa.pub`是公匙，可以放心告诉别人

###### 2. GitHub设置SSH KEY
登录GitHub，找到设置中的SSH KEY选项，把` id_rsa.pub `中的内容复制进` KEY `中

###### 3. 创建仓库
登录GitHub创建仓库，并把仓库地址复制下来

###### 4.添加远程库
`` git remote add origin <REMOTE_URL>
 ``

###### 5. 将本地内容推送到远程库
`` git push -u origin master ``

###### 6.本地提交命令
`` $ git push origin master ``

###### 7. 删除远程库
先查看远程库信息
`` $ git remote -v
origin  git@github.com:michaelliao/learn-git.git (fetch)
origin  git@github.com:michaelliao/learn-git.git (push) ``

###### 8.根据名称删除远程库地址
`` $git remote rm origin ``