# perun-ansible-apache2

Ansible galaxy role cesnet.apache2 that installs Apache2 and configure websites.

## Requirements


## Role variables
* apache_packages - List of packages which will be installed
* apache_modules - List of Apache2 modules which will be enabled
* apache_remove_sites - List of sites for remove
* apache_create_sites - List of sites which will be copied from templates (Must start with sites-available/ and end without .jinja2)
* apache_enable_sites - List of sites which will be enabled

## Available tags
* install
* configure
* start
* stop

## Example playbook
```
- hosts: all
  remote_user: root
  vars:
    - apache_packages:
        - apache2
    - apache_modules: []
    - apache_remove_sites: []
    - apache_create_sites: []
    - apache_enable_sites: []
  roles:
    - cesnet.apache2
```