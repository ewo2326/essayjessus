Common
======

This role helps to install some common and extra packages.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    common:
      packages:
        - netdiag
        - ruby

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: common, tags: common }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
