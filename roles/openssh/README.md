Openssh
=======

This role helps to install and configure openssh-server and openssh-client.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    ssh_port: 2288
    ssh_address:
      - 10.1.5.1
      - 10.1.5.2
    ssh_match_address:
      - name: permit_root_login_yes
        ip:
          - 10.20.1.10
          - 10.20.1.11
        host:
          - app1.example.com
          - app2.example.com

Variables 'ssh_port' and 'ssh_address' are optional.
Default values for optional variables:

    ssh_port: 22
    ssh_address:
      - 0.0.0.0

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: openssh, tags: openssh }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
