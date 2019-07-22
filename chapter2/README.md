# 客户端安装

本章介绍客户端安装

# 环境准备

操作系统：
Ubuntu 16.04

| 需要安装的软件 | 版本
| ------ | ------ |
| Node.js | v10.15.0 |
| cnpm | * |

具体步骤
1：安装curl，**sudo apt install curl**  
2：安装NVM，**curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash**  
3：安装Node.js，**nvm install v10.15.0**  
4：安装cnpm，**npm install -g cnpm --registry=https://registry.npm.taobao.org**  
6：下载项目工程，**git clone git@github.com:RippleBc/EasyBc.git**  
7：进入项目文件，**cnpm install**  

# 配置
打开项目工程目录下的**client**目录下的**nodes.json**文件，如下图所示  
![配置文件](/asserts/5.bmp "配置文件")  

默认的配置文件是我们推荐的可信任的UNL节点信息，当然用户可以自由地选择UNL节点信息  

# 启动

1：编译客户端代码，执行命令**npm run build_transaction_client**
2：运行transaction server，执行命令**npm run transaction_server**

![客户端](/asserts/6.bmp "客户端")  