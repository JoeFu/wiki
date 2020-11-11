# Laravel


## Laravel 常用命令

    php artisan key:generate 加密服务，生成key
    php artisan  migrate  迁徙数据库
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

### Laravel    清理 缓存 和 配置


    php artisan cache:clear
    php artisan route:clear
    php artisan config:clear
    php artisan view:clear



    




