Mysql-server
============

This role helps to install and configure standalone mysql server.

Requirements
------------

This role requires ansible 1.4 or higher.  
Before running this role, you have to create a password file and encrypt it with vault.  
Location for the password file is '\<playbook_dir\>/vars/secrets/mysql/\<inventory_hostname\>/\<username\>'.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    mysql_datadir: /var/lib/mysql
    mysql_bind_address: 127.0.0.1

Variables 'mysql_datadir' and 'mysql_bind_address' are defaults.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: mysql-server, tags: mysql-server }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
