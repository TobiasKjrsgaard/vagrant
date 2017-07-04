# Apache Role
Ansible role that installs the latest version of Apache 2 web server, including docs and utils and mod_rewrite, from Ondřej Surý's [PPA-repository](https://launchpad.net/~ondrej/+archive/ubuntu/apache2) on Ubuntu machines.

Installed packages:
- apache2
- apache2-doc
- apache2-utils

## Tasks
* Install Apache 2.4 packages
* Enable `mod_rewrite` in Apache 2.4
* Configure default server in `/var/www/html`
* Enable/disable `default` and `default_ssl` sites
