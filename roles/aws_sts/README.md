Aws_sts
=======

This role helps to assume a role using aws security token service and obtain temporary credentials

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    aws_access_key: "AKIAIOSFODNN7EXAMPLE"
    aws_secret_key: "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY"
    role_arn: "arn:aws:iam::9992233874612:role/production"
    role_session_name: "example"
    region: "us-east-1"
    mfa_serial_number: "arn:aws:iam::935170375193:mfa/user"
    mfa_token: "173267"

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: aws_sts, tags: aws_sts }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
