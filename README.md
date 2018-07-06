

环境VS2013 + Ubuntu 14.10

1、使用了版本1.0.14

http://nginx.org/download/nginx-1.0.14.tar.gz

2、先在Ubuntu中编译，执行以下命令。编译并产生配置文件。方便在VS中调试。

```c
./configure
sudo make 
sudo install
```

3、修改文件夹权限，设置端口，端口转发等

```c
sudo chmod -R 777 /usr/local/nginx
sudo chmod -R 777 /usr/local/nginx/conf
sudo chmod -R 777 /usr/local/nginx/logs
sudo chmod -R 777 /usr/local/nginx/sbin
```

/usr/local/nginx/conf/nginx.conf 修改以下信息

```c
listen       8088;
```

/usr/local/nginx/conf/nginx.conf 添加以下信息

```c
daemon off;
master_process off;
```

4、VS2013编译，设置断点调试。





