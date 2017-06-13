Ec2_vpc_public
==============

This role helps to create ec2 instance with extra added volumes (managed via public ip).

Requirements
------------

This role requires ansible 1.4 or higher.

Role Variables
--------------

The variables that can be passed to this role and a brief description about them are as follows:

    keypair: example
    instance_type: c3.xlarge
    private_ip: 10.10.0.20
    public_ip: 52.28.220.137
    security_group: [default,http,ssh]
    vpc_subnet_id: subnet-fc8e0695
    image: ami-1a494507
    region: eu-central-1
    zone: eu-central-1a
    aws_access_key: "AKIAIOSFODNN7EXAMPLE"
    aws_secret_key: "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY"
    ec2_url: "https://ec2.amazonaws.com"
    ebs_optimized: yes
    instance_profile_name: app
    mail_from: admin@example.com
    mail_to: admin@example.com
    volumes:
      - device_name: /dev/xvdb
        volume_size: 80
        device_type: gp2
        ephemeral: ephemeral0
    volumes_mount:
      - device_name: /dev/xvdb
        mount_point: /data
        mount_options: defaults,rw,relatime,nodiratime,noatime
        mount_passno: 2
        mount_point_owner: www-data
        mount_point_group: www-data

Variable 'volumes_mount' is not obligatory.  
Variables 'ebs_optimized', 'instance_profile_name', 'volumes' and 'mail_from' are optional.  
Default values for optional variables:

    ebs_optimized: no
    instance_profile_name: ''
    volumes: ''
    mail_from: ansible@project.org

Change root device size:

    volumes:
      - device_name: /dev/xvda
        volume_size: 500
        device_type: gp2

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: ec2_vpc_volumes_public, tags: ec2_vpc_volumes_public }

License
-------

BSD

Author Information
------------------

Created by Viacheslav Kuzmenko (oxygen@zeoalliance.com)
