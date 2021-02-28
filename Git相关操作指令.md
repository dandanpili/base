### 将本地仓库上传到github并相互关联，例子：与base仓库关联

先在本地将要上传的文件夹内唤出gitBash

① git init （将该文件夹设为git管理的文件夹）

② git add . （将该文件夹下的所有文件都添加进暂存区）

③ git commit -m '第一次提交' （将文件提交到本地master分支上）

④ git remote add origin https://github.com/dandanpili/base.git 

⑤ git branch -M master

⑥ git push -u origin master （第二次开始，可以通过git push origin master将代码推送到git hub）

###  将github上的项目导入本地 

① git clone https://github.com/dandanpili/base.git （后面的https为github连接）