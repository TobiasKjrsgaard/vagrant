# Apache Sites role
Ansible role that creates apache virtual hosts in the `www_root` directory with a simple index page.

## Tasks
* Create site root directories in `www_root`
* Create a simple `index.html` page in the doc root
* Create and enable Apache configuration file for the site

## Default Configuration
```yaml
# Define machine variables
www_root: /var/www
www_user: vagrant
www_group: www-data

# Define virtual hosts for Apache
virtualhost_sites:
  - host: "{{ hostname }}.local | default(vagrant.local)"
```
