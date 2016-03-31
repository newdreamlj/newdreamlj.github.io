---
layout: post
title:  shadowsocks for ubuntu
---

###install shadowsocks under ubuntu

1. sudo apt-get update

2. sudo python --version

3. apt-get install python-gevent python-pip

4. pip install shadowsocks

5. sudo find / -name shadows*

6. 修改config.js

{

"server":"127.0.0.1",
"server_port":8388,
"local_port":10808,
"password":"bgt56yhn",
"timeout":600,
"method":null

}

7. 后台长期启动shadowsockts

nohup ssserver -c /etc/shadowsocks/config.json > log &

查看后台启动任务： jobs

关掉 fg %n

 

8. 开机自动启动：

cd /etc/

sudo vim rc.local

加上一行：

/usr/local/bin/ssserver -c /etc/shadowsocks/config.json

 

9. 配置客户端：

{
"server":"0.0.0.0",
"server_port":8388,
"local_port":10808,
"password":"bgt56yhn",
"timeout":600,
"method":null
}

 

SHADOWSOCKS 服务端部署