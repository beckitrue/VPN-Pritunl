vpn-install-pritunl
=========

Installs, starts, and enables Pritunl and MongoDB on an AWS EC2 instance running Oracle Linux

Requirements
------------

yum

yum_repository

service

gpg keys

Role Variables
--------------
None as currently written. 

Dependencies
------------

Ansible 2.8 - yum lock_timeout

AWS EC2 instance running Oracle Linux ami - set in the group_vars/all file

Pritunl

MongoDB

Example Playbook
----------------

    - hosts: vpn-server
      roles:
         - vpn-install-pritunl

License
-------

BSD

Author Information
------------------

Becki True
becki@beckitrue.com
