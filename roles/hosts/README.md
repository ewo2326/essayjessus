Hosts
=====

This role helps to configure the /etc/hosts file.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    hosts:
      - ip: 64.15.147.54
        host: rodc1.zeo.lcl
        comment: rodc servers
      - ip: 198.72.110.60
        host: rodc2.zeo.lcl
      - ip: 10.55.1.4
        host: git.zeo.lcl
        comment: repositories
      - ip: 10.55.1.4
        host: svn.zeo.lcl
      - ip: 10.55.10.44
        host: gitlab.zeo.lcl

The 'comment' variable is not obligatory.  
You can use the value 'empty' in comment variable to add a blank line.

Some instances with zabbix-proxy or other monitoring tools needs hosts_custom option:

    hosts_custom: yes

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hosts, tags: hosts }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
