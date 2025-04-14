# ansible101

![Ansible Logo](https://github.com/nadmax/ansible101/blob/master/assets/ansible.jpg)

**This document is the complete version with every Ansible feature explained.**  

Below is a list of the current state of feature explanations:


## Inventory
An Ansible inventory is a list or group of host name lists used to automatically manage tasks on nodes in your infrastructure.  
Inventory can be passed at command line, but it is recommanded to create an inventory files.  
Default location for the inventory file is ``/etc/ansible/hosts``, but you can specify a different one at the command line using the ``-i <filepath>`` option or in the configuration system located at ``/etc/ansible/ansible.cfg`` 

[View a simplest inventory file example here](https://github.com/nadmax/ansible101/blob/master/inventory/hosts.cfg)
[View a complex inventory file example here](https://github.com/nadmax/ansible101/blob/master/inventory/complex.yaml)

## Playbooks
Playbooks are automation blueprints that Ansible uses to deploy and configure nodes in an inventory.  
They cover different use cases such as:
- Executing tasks with elevated privileges or as a different user.
- Using loops to repeat tasks for items in a list.
- Delegating playbooks to execute tasks on different machines.
- Running conditional tasks and evaluating conditions with playbook tests.
- Using blocks to group sets of tasks.

They are represented in YAML format.  

[View a playbook file example here](https://github.com/nadmax/ansible101/blob/master/playbooks/example.yaml)