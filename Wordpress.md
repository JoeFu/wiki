# Wordpress


## 常见故障

### 上传文件的时候出现 服务器 Internal 500 故障
先尝试使用如下命令，并检查 php.ini配置 

    chown -R centos:centos /var/lib/nginx   

