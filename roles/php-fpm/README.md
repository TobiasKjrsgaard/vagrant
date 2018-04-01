# PHP-FPM Role
Ansible Role that installs PHP 7.1 packages from Ondřej Surý's [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/php) on Ubuntu machines, including command-line interface and various other libraries and utilities.

Installed packages:

- php7.1-cli
- php7.1-common
- php7.1-curl
- php7.1-dev
- php7.1-fpm
- php7.1-gd
- php7.1-mbstring
- php7.1-mcrypt
- php7.1-mysql
- php7.1-opcache
- php7.1-xml
- php7.1-xmlrpc
- php7.1-zip

## Tasks
* Add Ondřej Surý's [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/php)
* Install PHP 7.1 packages for FPM and CLI use
* Configure max file upload size and various error logging settings

## Default Configuration

```yaml
# Specify the maximum size of file uploads and request bodies
max_file_upload_size: 10M

# PHP error reporting and logging settings for a standard production environment
php_error_reporting: 'E_ALL & ~E_DEPRECATED & ~E_STRICT'
php_display_errors: 'Off'
php_log_errors: 'On'

# Disable the default `www.conf` FPM pool
disable_default_pool: false
```
