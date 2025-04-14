# Inventory
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