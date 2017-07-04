# NGiNX WordPress Site Role
Ansible role that creates Nginx virtual hosts in the `www_root` directory and sets up a `wp-cli.yml` configuration files that makes it easy to install WordPress from the command line.

## Tasks
* Install [WP-CLI](http://wp-cli.org/) with bash completions
* Create site root directories in `www_root`
* Create PHP-FPM pools for individual sites
* Create and enable nginx configuration file for the site
* Create WP-CLI configuration file in site root directory
* Download [WordPress](https://wordpress.org/) core files and set up database connection.

## Default Configuration
```yaml
# Specify where html and log directories should be located
www_root: /var/www
www_user: vagrant
www_group: www-data

# Specify the maximum size of file uploads and request bodies
max_file_upload_size: 10M

# Specify where WP-CLI should be downloaded from and where it should be installed
wp_cli_url: https://raw.github.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
wp_comp_url: https://raw.github.com/wp-cli/wp-cli/master/utils/wp-completion.bash
bin_path: /usr/bin/wp
comp_path: /etc/bash_completion.d/
```
