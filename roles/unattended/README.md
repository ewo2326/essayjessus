Unattended
==========

This role helps to install and configure unattended upgrade.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    unattended:
      blacklist:
        - php5
        - php-pear
        - mysql-client
        - mysql-server
        - mongodb-10gen

Variable 'unattended.blacklist' is default.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: unattended, tags: unattended }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
