# role-zabbix-5
The Enterprise-Class Open Source Network Monitoring Solution

Example(s)
----------------

# Zabbix server (Ubuntu 20.04lts AMD64)
```
- hosts: zabbix-server
  become: yes

  vars:
    # -- roles/role-zabbix-5 --
    zbx_type : 'server'  # Set zabbix type to "server".

  roles:
    - app-cert-selfsigned
    - role-apache2
    - role-mariadb-server-10.5
    - role-zabbix-5

  tasks:
```
