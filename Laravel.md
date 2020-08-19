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

    




