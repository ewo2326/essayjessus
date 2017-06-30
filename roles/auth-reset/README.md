Auth-reset
===============

This role lock password and change ssh key for root user, and delete user admin (include home folder).

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: auth-reset, tags: auth-reset }

License
-------

BSD

Author Information
------------------

Created by Vilen Virzhakovskiy (knyaz@zeoalliance.com)
