Sudo
====

This role helps to install and configure sudo.

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    sudo:
      - file: unix-admins
        groups:
          - UNIXadmin
        command: ALL=(ALL:ALL) ALL
        state: present
      - file: admins
        groups:
          - "{{ inventory_hostname }}-root"
        command: ALL=(ALL:ALL) ALL
        state: present
      - file: webdev
        groups:
          - "{{ inventory_hostname }}-www"
        command: ALL=(www-data) /bin/bash
        state: present
      - file: elenka
        users:
          - elenka
        command: ALL=(ALL:ALL) ALL
        state: present
      - file: deployment
        users:
          - chumakser
          - gusto
        command: ALL=(ALL) /usr/bin/dmb,/usr/bin/apt-cache policy megabackup-*
        state: present
      - file: nopasswd
        groups:
          - sudo
        command: "ALL=(ALL) NOPASSWD: ALL"
        state: present

Variable 'state' is optional.
Default values for optional variables:

    sudo:
      - file: unix-admins
        groups:
          - UNIXadmin
        command: ALL=(ALL:ALL) ALL
        state: present

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: sudo, tags: sudo }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
