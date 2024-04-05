Prebuild php zip extension for CentOS

## Install remi-php82

```bash
yum-config-manager --enable remi-php80
sudo yum install -y php php-common php-cli

sudo alternatives --set php /usr/bin/php
php -v
```

## Fix zip extension issue

```bash
pecl uninstall zip
pecl install zip
# if has error with zipconf.h
cp /usr/local/lib/libzip/include/zipconf.h /usr/local/include/zipconf.h
pecl install zip
```
