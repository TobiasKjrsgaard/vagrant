# MariaDB Database Server Role
Ansible role that installs and configures the latest version of [MariaDB](https://mariadb.org) MySQL database server from DigitalOcean's mirror server in The Netherlands.

## Tasks
* Add MariaDB apt repository
* Install `mariadb-server` apt package
* Set MySQL server root user password
* Delete anonymous database user and test table
* Create databases defined in `mysql_databases` var
* Create users defined in `mysql_users` var

## Database and User creation syntax
```yaml
# List of databases to be created (optional)
mysql_databases:
  - name: foobar
    collation: "utf8_general_ci"        # optional, defaults to "utf8_general_ci"
    encoding: "utf8"                    # optional, defaults to "utf8"

# List of users to be created (optional)
mysql_users:
  - name: baz
    pass: pass
    priv: "*.*:ALL"                     # optional, defaults to "*.*:ALL"
    host: "%"                           # optional, defaults to "localhost"

```
