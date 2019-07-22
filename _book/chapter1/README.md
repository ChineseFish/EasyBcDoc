# 服务器部署

<h2 style="color:red">如果不需要部署自己的UNL节点，可以跳过该小结,我们提供了默认的诚实的UNL节点。</h2>

本章介绍服务器部署的相关知识

# 环境准备

操作系统：
Ubuntu 16.04

| 需要安装的软件 | 版本
| ------ | ------ |
| Node.js | v10.15.0 |
| cnpm | * |
| pm2 | 3.2.9 |
| mysql | 8.0.15 |
| mongo | 4.0.10 |

具体步骤
1：安装curl，**sudo apt install curl**  
2：安装NVM，**curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash**  
3：安装Node.js，**nvm install v10.15.0**  
4：安装cnpm，**npm install -g cnpm --registry=https://registry.npm.taobao.org**  
5：安装pm2，**cnpm install -g pm2@3.2.9**  
6: 安装mysql 8.0.15（具体安装步骤请参考mysql官网）
7：安装mongo 4.0.10（具体安装步骤请参考mongodb官网）
8：下载项目工程，**git clone git@github.com:RippleBc/EasyBc.git**  
9：进入项目文件，**cnpm install**  

# 启动

1：进入项目目录EasyBc，执行命令**pm2 start**  
2：执行命令**pm2 logs**，如果出现如下图片则表示节点启动成功。  

![启动成功](/asserts/4.bmp "启动成功")

# 配置
1：编译客户端代码，执行命令**npm run build_monitor_client**
2：运行monitor server，执行命令**npm run monitor_server**
3：打开网页，**http://localhost:8083**，初始账号密码为**admin**
4: 配置节点信息，如下图所示
![配置节点信息](/asserts/3.bmp "配置节点信息")
5：点击查看详情，进入具体节点的配置页面，点击左侧菜单栏配置节点信息，如下图所示
![配置节点信息](/asserts/3.bmp "配置节点信息")