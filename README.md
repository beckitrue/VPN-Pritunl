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

Ansible 2.8 - yum lock_timeout

This playbook has vault encrypted strings in the group_vars/all file. The playbook has to be called with the --vault-password-file option or edit /etc/ansible/ansible.cfg file with the password file name.

Example Playbook
----------------

Run in this order. Some steps are still manual.

    ansible-playbook site.yml 
    get setupkey from message log
    Use browser https://<ip> and use setup key to login
    ansible-playbook -i "<ip>", pritunl-default-password.yml
    username and password will be in message log

Login and set up databse after installation. Can't get the default password until you do. Here's a video of the whole process: https://youtu.be/sN_6ZELmyWM

Configuration documentation 
https://docs.pritunl.com/docs/configuration-5

Pritunl commands 
https://docs.pritunl.com/docs/commands


Things to do
----------------

* Use dynamic inventory
https://docs.ansible.com/ansible/latest/user_guide/intro_dynamic_inventory.html#inventory-script-example-aws-ec2

* Automate Pritunl configuration

License
-------

BSD

Author Information
------------------

Becki True
becki@beckitrue.com
