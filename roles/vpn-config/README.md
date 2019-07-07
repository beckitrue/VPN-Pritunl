vpn-config
=========

Configures the Pritunl VPN server created by other roles

Requirements
------------

blockinfile

shell

yum

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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: vpn-server
      roles:
         - vpn-config

License
-------

BSD

Author Information
------------------

Becki True
becki@beckitrue.com
