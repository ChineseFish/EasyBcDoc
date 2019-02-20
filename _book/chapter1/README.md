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

具体步骤
1：安装curl，**sudo apt install curl**  
2：安装NVM，**curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash**  
3：安装Node.js，**nvm install v10.15.0**  
4：安装cnpm，**npm install -g cnpm --registry=https://registry.npm.taobao.org**  
5：安装pm2，**cnpm install -g pm2@3.2.9**  
6：下载项目工程，**wget https://github.com/ChineseFish/EasyBcZip/raw/master/EasyBc_v1.0.0.zip**  
7：解压，**unzip EasyBc_v1.0.0.zip**  
8：进入项目文件，**cnpm install**  

# 配置

打开项目工程目录下的**server**目录下的**nodes.js**文件如下图所示
![配置](/asserts/3.bmp "配置")  

1：红色方块中添加的是UNL中其它Server节点的**URL地址**以及**公钥地址**。  
2：蓝色方块中port表示本地Server节点开放的**端口**以及**URL地址**（如果服务器仅有一个IP地址，为空即可）。  
3：黄色方块中privateKey表示本地Server节点的**私钥地址**，address表示**公钥地址**。  

上述内容请务必正确填写

# 启动

1：进入项目目录EasyBc_v1.0.0，执行命令**pm2 start server/index.js**  
2：执行命令**pm2 logs**，如果出现如下图片则表示节点启动成功。  

![启动成功](/asserts/4.bmp "启动成功")