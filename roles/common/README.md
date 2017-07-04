# Common Housekeeping Role
Ansible role that does basic housekeeping tasks on Ansible-managed hosts.


## Tasks
* Update apt-get cache and upgrade all packages to latest version
* Install commonly used apt software packages (see list below)


## Installed Packages
- build-essential
- python
- git
- curl
- rsync
- ruby
- rmate


## Default Configuration
```yaml
# Enable to ensure all packages are kept up to date
common_apt_upgrade: true
```
