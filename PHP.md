# PHP 


## Mac 卸载旧版本的 PHP

    查看旧版本 php -version; Eg. PHP72
    brew services stop php72
    brew uninstall php72
    brew unlink php72
    brew cleanup
    sudo rm -rf /usr/local/Cellar/php72*
    sudo rm -rf /usr/local/opt/php72* 
    sudo rm -rf /usr/local/var/homebrew/linked/php72*
    sudo rm -rf /usr/local/etc/php/
    sudo rm -rf /etc/php*.ini /etc/php-*
    sudo rm -rf /usr/local/bin/pear
    sudo rm -rf /usr/local/bin/peardev
    sudo rm -rf /usr/local/bin/pecl
    sudo rm -rf /usr/local/bin/phpdbg
    sudo rm -rf /usr/local/include/php/
    sudo rm -rf /usr/bin/php*
    brew prune

## Mac 安装全新的 PHP 版本

    brew install php
    或者指定版本: brew install php72

