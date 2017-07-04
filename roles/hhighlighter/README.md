# Highlighter Role
Ansible role that installs `ack` and `h` commands on Ubuntu machines.

## Tasks
* Install ack-grep packages and create `ack` alias in the global `/etc/bash.bashrc` file
* Install [hhighlighter](https://github.com/paoloantinori/hhighlighter) script and source it in the global `/etc/bash.bashrc` file
* Create `logacc()`, `logerr()` and `logphp()` bash-functions for for watching highlighted logfiles

## Default Configuration
```yaml
h_url: https://raw.githubusercontent.com/paoloantinori/hhighlighter/master/h.sh
h_path: /usr/local/lib/h.sh
```
