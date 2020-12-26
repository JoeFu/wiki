# Laravel


## Laravel 常用命令

    php artisan key:generate 加密服务，生成key
    php artisan migrate  迁徙数据库
    php artisan migrate:rollback
    php artisan migrate:fresh

    php artisan make:seeder  添加数据库Seeder
    php artisan db:seed --class=SnTableSeeder 数据库填充数据库


## Laravel  进入维护模式

### Maintenance Mode

    php artisan down
    php artisan down --message="Upgrading Database" --retry=60
    php artisan down --allow=127.0.0.1 --allow=192.168.0.0/16   (允许特定IP访问)
    php artisan up （重新上线）



### Composer Out of Memory while using require xxxx

    COMPOSER_MEMORY_LIMIT=-1 composer require intervention/image


### If Laravel 'Please provide a valid cache path.'
    cd storage/
    mkdir -p framework/{sessions,views,cache}
    chmod -R 777 framework

### Class 'xxxx' not found
    Run:
    composer install

### Laravel Optimise

    composer dump-autoload

### 优化 Laravel 配置/刷新配置


    php artisan cache:clear
    php artisan route:clear
    php artisan config:clear
    php artisan view:clear
    php artisan optimize

### 显示所有路由配置

    php artisan route:list    

## Laravel 配置 JWT

#### Install JWT package via composer
    composer require tymon/jwt-auth
#### Publish the config
    php artisan vendor:publish --provider="Tymon\JWTAuth\Providers\LaravelServiceProvider"
#### Generate secret key
    php artisan jwt:secret


#### Configure Auth guard inside the config/auth.php
        
        'defaults' => [
        'guard' => 'api',
        'passwords' => 'users',
        ],


            'guards' => [
        'web' => [
            'driver' => 'session',
            'provider' => 'users',
        ],

        'api' => [
            'driver' => 'jwt',
            'provider' => 'users',
            'hash' => false,
        ],
    ],
#### Update User model

    /app/User.php
    class User extends Authenticatable implements JWTSubject

ADD:
    public function getJWTIdentifier()
    {
        return $this->getKey();
    }
Create AuthController

    php artisan make:controller AuthController

## 在 Laravel 7 中使用 UUID

参考此文章[链接](https://learnku.com/laravel/t/44937)

## 在 Laravel 中使用 AWS S3 存储系统

参考此文章 [Getting started with Amazon S3 storage in Laravel](https://dev.to/aschmelyun/getting-started-with-amazon-s3-storage-in-laravel-5b6d)

