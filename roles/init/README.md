# Initialization role
Ansible role that does a basic setup of new machines to ensure a proper environment.


## Tasks
* Update information on available packages in the apt cache
* Install commonly used apt software packages (see list below)
* Set machine hostname to `hostname` variable if defined
* Set current timezone to `init_timezone` variable if defined
* Generate locales listed in the `init_locales` variable
* Create users and groups specified in `init_users` variable
* Authorize `~/.ssh/id_rsa.pub` key from host machine for created users


## Installed Packages
- ntp
- build-essential
- git
- curl
- rsync
- ruby
- dbus
- libnss-myhostname
- rmate


## Default Configuration
````yaml
# System wide settings for timezone, locale, etc.
init_timezone: 'UTC'
init_locales:
  - 'en_US.UTF-8'

# List of users to be created
# init_users:
#   - name: deploy
#     groups: adm,sudo
````
