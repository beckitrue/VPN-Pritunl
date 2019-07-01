vpn-install-pritunl
=========

Installs, starts, and enables Pritunl and MongoDB on an AWS EC2 instance running Oracle Linux

Requirements
------------

yum
yum_repository
shell
service
gpg keys

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------
None as currently written. 

Dependencies
------------

AWS EC2 instance running Oracle Linux ami - set in the group_vars/all file
Pritunl
MongoDB

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

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
