# NGiNX Server Role

Install the latest version *stable* version of the [nginx](http://nginx.org/) web server from Ondřej Surý's nginx [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/nginx) and do some basic configuration.

## Tasks

* Add Ondřej Surý's nginx [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/nginx).
* Install latest version of the `nginx` package.
* Create `/var/www/html/` and `/var/www/log` directories for the default server.
* Copy configuration files for setting up a default server in `/var/www` directory.
* Optionally disable the default server if `disable_default_site` is `true`.

## Default Configuration

```yaml
# Determine where the www directory should be located
www_root: /var/www
www_user: www-data
www_group: www-data

# Disable the default site
disable_default_site: false

# Enable use of sendfile() in NGiNX
nginx_disable_sendfile: false
```
