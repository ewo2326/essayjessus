Common-prod
===========

This role is a common meta role for production environment.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

None

Dependencies
------------

Roles:
- hostname
- hosts
- openssh
- skel
- motd
- locale
- timezone
- ntp
- ulimit
- sudo
- postfix
- sources-list
- common
- unattended
- postinstall
- logwatch
- ssh_keys
- appdeploy

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: common-prod, tags: common-prod }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
