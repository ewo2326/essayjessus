Preprovision
============

This role helps to preprovision ec2 or any other instance.
This role include tasks from hosts, hostname, libnss-ldapd and sudo roles.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

None

Dependencies
------------

Roles:
- cloudmccloud-list (optional)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: preprovision, tags: preprovision }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
