Icinga
=========

Installs and configures Icinga 2 on Debian systems.

Requirements
------------

None.

Role Variables
--------------

 * icinga2_modules: Icinga modules to enable
 * icinga2_repository: Debian repository to use for Icinga packages
 * icinga2_admin_username: Username for administrator account
 * icinga2_plugin_custom_dir: directory where your custom check plugins are located
 * icinga2_unwanted_files: config files you want to remove
 * icinga2_users: list of users to whom send notifications, see the example playbook.
 * mysql_health_checks: TODO

Dependencies
------------

 * ajsalminen.apt_source
 * ajsalminen.mysql_sync
 * ajsalminen.mysql_database
 * ANXS.mysql

Example Playbook
----------------

```
- hosts: icinga
  roles:
    - role: icinga2
      icinga2_users:
        - username: tester
          email: example@example.com
```

License
-------

MIT

Author Information
------------------

Libraries.fi
