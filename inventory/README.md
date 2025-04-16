# Inventory

## The Basics
An Ansible inventory is a list or group of host name lists used to automatically manage tasks on nodes in your infrastructure.  
You can create your inventory file in one of many formats.  
The most common formats are INI and YAML, as they are built-in.  

A basic INI might look like this:
```ini
# ==== Web Server Group ====
[webservers]
web1.example.com     # First web server
web2.example.com     # Second web server

# ==== Database Server Group ====
[dbservers]
db1.example.com      # Database server
```

Inventory can be passed at command line, but it is recommanded to create an inventory files.  
Default location for the inventory file is ``/etc/ansible/hosts``, but to specify a different one at the command line, use the ``-i <filepath>`` option.  
You can also configure Ansible Inventory path by creating a file called ``ansible.cfg`` at your project root.  
  
Here's how it might look:
```conf
[defaults]
inventory = inventory/simple.ini
```


Two commands example related to inventory:  
```bash
ansible-inventory -i inventory/simple.ini --list # Show simple.ini inventory information, including hosts info
ansible webservers -m ping -i inventory/simple.ini # Ping the webservers group in the inventory simple.ini located at inventory folder
```