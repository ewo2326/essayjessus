Timezone
========

This role helps to set timezone.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    timezone: America/New_York

Variable 'timezone' is default.

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: timezone, tags: timezone }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
