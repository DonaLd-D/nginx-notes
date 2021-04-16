nginx使用指南

1 安装nginx
    1 ssh root@your ip //连接云服务器
    2 yum install yum-utils //安装yum-utils
    3 vim /etc/yum.repos.d/nginx.repo //配置repo
    4 yum list|grep nginx //查看nginx的版本
    5 yum install nginx //安装nginx
    6 nginx -v //查看nginx的版本

2 nginx常用命令
    1 /usr/sbin/nginx //启动nginx
    2 nginx -h //帮助命令
    3 nginx -c //制定某个文件
    4 nginx -t //测试
    5 nginx -v //打印版本
    6 nginx -V //打印详细版本
    7 nginx -s stop //立即停止nginx
    8 nginx -s quit //优雅停止
    9 nginx -s reload //重载
    10 nginx -s reopen //更换日志文件
    11 whereis nginx //查看nginx在哪个目录

3 验证是否启动nginx
    1 /usr/sbin/nginx
    2 ps -aux |grep nginx //看进程
    3 your ip:80 //访问网站

4 配置文件
    1 语句以;结尾
    2 用{}组织多条指令
    3 用include引入
    4 用#注释
    5 用$表示变量

5 搭建静态服务器
    scp -r 文件目录 root@your ip:/usr/share/nginx/web/ //上传静态资源至服务器某个目录，然后在nginx.conf引入的default.conf里配置上传的静态页面

