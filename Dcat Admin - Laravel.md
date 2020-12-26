# 开发部分

## 安装

### 安装环境

        PHP >= 7.1
        Laravel 5.5.0 ~ 8.*
        Fileinfo PHP Extension

### 安装 Laravel 框架        

        composer create-project --prefer-dist laravel/laravel 项目名称
### 配置数据库

        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=
        DB_USERNAME=
        DB_PASSWORD=


### 安装 Dcat Admin
        
        composer require dcat/laravel-admin:"2.0.10-beta"
        php artisan admin:install
        php artisan admin:publish --assets --force
        php artisan admin:publish --migrations --force # 表结构有变动
        php artisan migrate

### 如遇到安装内存不足的情况 composer 前 添加：
        
        COMPOSER_MEMORY_LIMIT=-1 composer xxxx....


# 部署部分


## Web 目录指向 public，Nginx上加上伪静态

        location / {
            try_files $uri $uri/ /index.php?$query_string;
        }



# 数据库



## 生成迁移

使用　make:migration Artisan 命令 命令来创建迁移：
    
    php artisan make:migration create_users_table


## Migrate 数据库迁移

        php artisan migrate


# 其他

### 修改Footer 

Path:

- vendor/dcat/laravel-admin/resources/views/layouts/vertical.blade.php

###  Github 出现冲突


解决本地冲突 

        git reset --hard
        git clean -d -f