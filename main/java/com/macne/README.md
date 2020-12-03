This is test git for github

上传代码到github步骤
1:下载git
2:github创建repo
3:到settting中选择SSH and GPG keys创建id_rsa.pub
4:git中使用ssh-keygen -t rsa -C "yourname@youremail"创建key
5:github中粘贴id_rsa.pub 新建成功后系统会向邮箱发送一封邮件
5:使用ssh密钥ssh -T git@github.com 连接github
6:如果出现Permission denied (publickey)问题 先删除.ssh
7:rm -r ~./ssh
8:重新使用ssh-keygen -t rsa -C "yourname@youermail"创建key
9:添加使用权限
10:chmod 0700 ~/.ssh
11:chmod 0600 ~/.ssh/id_rsa
12:使用ssh -T git@github.com连接github
13:设置全局用户名及邮箱
14: git config --global user.name "youname"
15: git config --global user.email "youremail"
16：切换到需要上传的项目位置 
17: git init
18: git add .(上传全部文件到github)
19:使用git commit -m "yourcomment"
20: 添加远程仓库地址 (选择ssh) git remote add origin https://github.com/soloacfun/acsp.git

21:上传项目 git push -u origin master
22:如果远程仓库设置错误 使用 git remote rm origin 重新配置
上传项目 git push -u origin master


