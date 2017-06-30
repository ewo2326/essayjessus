Opendkim
========

!!! This role is deprecated, don't use it !!!   
This role helps to install and configure the opendkim.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    opendkim:
      email: root
      domains:
        - zeoalliance.com
        - cloudmccloud.com
      trusted:
        - mail1.cloudmccloud.com
        - mail2.cloudmccloud.com
      selector: mail

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: opendkim, tags: opendkim }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
