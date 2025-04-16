# ansible101

![Ansible Logo](https://github.com/nadmax/ansible101/blob/master/assets/ansible.jpg)

**This document is the complete version with each Ansible concept explained.**  
**Please refer to the list of concepts below if you want to see just one that interests you.** 

## Ansible concepts
🟢 Control node  
🟢 Managed nodes  
🟡 [Inventory](httpŝ://github.com/nadmax/ansible101/blob/master/inventory/README.md)  
🟡 [Playbooks](httpŝ://github.com/nadmax/ansible101/blob/master/playbooks/README.md)  
🔴 Roles  
🔴 Tasks  
🔴 Handlers  
🔴 Modules  
🔴 Plugins  
🔴 Collections  

## What is Ansible?
Ansible is an open-source infrastructure automation system, handling configuration management, application deployment, cloud provising, network automation and multi-node orchestration.  

Common use cases for Ansible are:  
- Eliminate repetition and simplify workflows
- Manage and maintain system configuration
- Continuously deploy complex software
- Perform zero-downtine rolling updates  

It uses SSH with existing OS credentials to access to remote machines, allowing it to be decentralized.

## Installation
To install Ansible, you need pip (Python's package manager).  
[See how to install Pip here](https://pip.pypa.io/en/stable/installation/)  

Once you have installed pip, run this to install Ansible:  
```bash
pip install ansible
```

## Control node
Control node refers to the machine from which you run the Ansible CLI tools.  
You can use any computer that meets the software requirements as control node (laptops, shared desktops, servers).  

## Managed nodes
Managed nodes refer to the target devices (servers, network appliances or any computer) you manage with Ansible.  
It is not recommended to install Ansible on managed nodes.  

## Inventory
*Note: there are many things to explain about Ansible Inventory.*  
*I cover here the basics.*  
*[Please refer to the complete guide here](https://github.com/nadmax/ansible101/blob/master/inventory/README.md)*  

An Ansible inventory is a list or group of host name lists used to automatically manage tasks on nodes in your infrastructure.  
Inventory can be passed at command line, but it is recommanded to create an inventory files.  

Default location for the inventory file is ``/etc/ansible/hosts``, but you can specify a different one at the command line using the ``-i <filepath>`` option or in the configuration system located at ``/etc/ansible/ansible.cfg``.  

Two commands example related to inventory:  
```bash
ansible-inventory -i inventory/simple.ini --list # Show simple.ini inventory information, including hosts info
ansible webservers -m ping -i inventory/simple.ini # Ping the webservers group in the inventory simple.ini located at inventory folder
```

[View a simple inventory file example here](https://github.com/nadmax/ansible101/blob/master/inventory/hosts.cfg)  
[View a complex inventory file example here](https://github.com/nadmax/ansible101/blob/master/inventory/complex.yaml)

## Playbooks
Ansible playbooks are automation blueprints that Ansible uses to deploy and configure nodes in an inventory.  
They cover different use cases such as:
- Executing tasks with elevated privileges or as a different user.
- Using loops to repeat tasks for items in a list.
- Delegating playbooks to execute tasks on different machines.
- Running conditional tasks and evaluating conditions with playbook tests.
- Using blocks to group sets of tasks.

They are represented in YAML format.  

[View a playbook file example here](https://github.com/nadmax/ansible101/blob/master/playbooks/example.yaml)