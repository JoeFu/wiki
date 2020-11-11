# Mysql

## CentOS 安装 MySQL（生产环境）

参考如下文章: [CentOS安装MySQL详解](https://juejin.im/post/6844903870053761037)

## 常用语句

    UPDATE sn_table SET status = 1 where CAST(sn_code as SIGNED)> '93499040000' && CAST(sn_code as SIGNED)< '934990401679' 更新代码
## MacOS 安装 MySQL (开发环境)
    
### 使用Brew 安装 MySQL

* 安装Brew：

```
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

    brew install mysql
    
```

