# PHP-FPM Role
Ansible Role that installs PHP 7.0 packages from Ondřej Surý's [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/php) on Ubuntu machines, including command-line interface and various other libraries and utilities.

Installed packages:

- php7.0-cli
- php7.0-common
- php7.0-curl
- php7.0-dev
- php7.0-fpm
- php7.0-gd
- php7.0-mbstring
- php7.0-mcrypt
- php7.0-mysql
- php7.0-opcache
- php7.0-xml
- php7.0-xmlrpc
- php7.0-zip

## Tasks
* Add Ondřej Surý's [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/php)
* Install PHP 7.0 packages for FPM and CLI use
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
