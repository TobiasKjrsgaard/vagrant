# Avahi Role
Ansible role that installs [Avahi](http://avahi.org) to enable [Bonjour](http://www.apple.com/support/bonjour/) compatible zero configuration mDNS service on the local network. It also sets up additional `CNAME` records using the [avahi-alias](https://github.com/asharpe/avahi-alias) script by GitHub user asharpe.

## Tasks
* Install the `avahi-daemon` and `python-avahi` packages
* Install asharpe's `avahi-alias` python script as service
* Reload configuration and ensure services are running
