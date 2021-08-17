# 一个简单的HTTP代理

## 参数说明

```sh
-h, --host 指定代理主机地址，默认0.0.0.0，代表本机任意ipv4地址
-p, --port 指定代理主机端口，默认8080
-l, --listen 指定监听客户端数量，默认10
-b, --bufsize 指定数据传输缓冲区大小，值为整型，单位kb，默认8
-d, --delay 指定数据转发延迟，值为浮点型，单位ms，默认1
```

## 简单使用

### 服务端

```sh
# 启动服务
[wcx@localhost ~]$ python simple_http_proxy.py --bufsize 64
[info] bind=0.0.0.0:8080
[info] listen=10
[info] bufsize=64kb, delay=1ms
```

> 注：Linux查看本机IP地址的命令为 ifconfig，Windows为ipconfig

### 客户端

电脑：打开网络和Internet设置 -> 代理 -> 手动设置代理 -> 配置代理服务器IP和端口号

手机：选择一个已连接的WIFI，修改该网络 -> 显示高级选项 -> 手动设置代理 -> 配置代理服务器IP和端口号

