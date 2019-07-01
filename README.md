Pritunl VPN on AWS Playbook
=========

Creates a Pritunl VPN running on a single AWS t2.micro instance. This is the free version of Pritunl for personal use.
https://docs.pritunl.com/docs/installation

Requirements
------------    

Python >= 2.6
boto

Oracle Linux ami. Current Oracle Linux ami: ami-043f63bd4fa486e8d

Site Variables
--------------

AWS access key - vault encrypted string
AWS secret key - valut encrypted string
EC2 key name
EC2 region
EC2 group
EC2 instance type
EC2 image
EC2 VPC subnet

Dependencies
------------

This playbook has vault encrypted strings in the group_vars/all file. The playbook has to be called with the --vault-password-file option

Example Playbook
----------------

Including an example of how to use your playbook(for instance, with variables passed in as parameters) is always nice for users too:

    ansible-playbook provision-ec2.yml --vault-password-file </path/vault-password-file>
    ansible-playbook site.yml 
    get setupkey from message log
    Use browser https://<ip> and use setup key to login
    ansible-playbook pritunl-default-password.yml
    username and password will be in message log

Login and set up databse after installation
Configuration documentation 
https://docs.pritunl.com/docs/configuration-5

Pritunl commands 
https://docs.pritunl.com/docs/commands


Things to do
----------------
Disable network interface source/dest check on EC2 network interface - not automated yet
Configure SSL Cert on server
Use dynamic inventory https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html#inventory-script-example-aws-ec2
Automate Pritunl configuration

License
-------

BSD

Author Information
------------------

Becki True
becki@beckitrue.com
