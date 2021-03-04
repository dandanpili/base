## 如何启动dubbo和zookeeper

1、先将两个压缩包解压

#### 启动zookeeper

1、在bin目录下输入cmd

2、输入：zkServer.cmd运行服务端

3、输入：zkCli.cmd运行客户端

#### 启动dubbo

1、要先启动zookeeper才能启动dubbo

#####  先将dubbo-admin打包

2、在dubbo-admin目录下输入cmd，唤起命令行

3、输入mvn clean package将dubbo-admin打包

4、完成后可以在dubbo-admin/target目录下看到dubbo-admin-0.0.1-SNAPSHOT.jar文件

##### 启动dubbo

5、跳转到dubbo-admin-0.0.1-SNAPSHOT.jar文件的目录下，通过cmd唤起命令行，

输入java -jar dubbo-admin-0.0.1-SNAPSHOT.jar 运行dubbo程序

6、在浏览器输入localhost:7001即可进入dubbo界面，用户名和密码均为root

