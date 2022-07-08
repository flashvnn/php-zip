Prebuild php zip extension for CentOS

## Fix zip extension issue

```bash
pecl uninstall zip
pecl install zip
# if has error with zipconf.h
cp /usr/local/lib/libzip/include/zipconf.h /usr/local/include/zipconf.h
pecl install zip
```
