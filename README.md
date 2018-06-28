# nginx+php+mysql+redis的部署

## 目录

1. [nginx的部署](#nginx的部署)
2. [php的部署](#php的部署)
3. [mysql的部署](#mysql的部署)
4. [redis的部署](#redis的部署)

## nginx的部署

### nginx简介

* Nginx是一款轻量级的Web 服务器/反向代理服务器

### 选择理由

* 可以快速部署负载均衡，以及拥有比apache更高的并发性能，也可搭配apache一起使用，两者并不存在竞争性

### 部署

* 获取nginx安装包并进行解压

```linux
#cd /usr/local
#wget http://nginx.org/download/nginx-1.10.3.tar.gz
#tar -zxvf nginx-1.10.3.tar.gz
```

* 进行编译前的环境测试以及配置，进行编译，进行安装(configure可进行更多选择配置，详见nginx官网配置指导)

```linux
#configure --prefix=/usr/local/nginx
#make
#make install
```

* 将nginx加入环境变量
  * 编辑/etc/profile
    ```linux
    #vi /etc/profile
    ```
  * 在最后一行添加以下内容
    ```shell
    PATH=$PATH:/usr/local/nginx/sbin 
    export PATH
    ```
* 启动nginx并测试
  * nginx启动
    ```linux
    #nginx
    ```

  * nginx端口查看
    ```linux
    #netstat -ltnp
    ```
  * 登录web查看，浏览器中输入`127.0.0.1`(本机测试使用127.0.0.1或者localhost，公网测试请输入相应ip)  
    ![nginx](https://github.com/FYKANG/create_environment/raw/master/img/nginx.png)

## php的部署

## mysql的部署

## redis的部署