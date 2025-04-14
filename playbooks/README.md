# Playbooks
Playbooks are automation blueprints that Ansible uses to deploy and configure nodes in an inventory.  
They cover different use cases such as:
- Executing tasks with elevated privileges or as a different user.
- Using loops to repeat tasks for items in a list.
- Delegating playbooks to execute tasks on different machines.
- Running conditional tasks and evaluating conditions with playbook tests.
- Using blocks to group sets of tasks.

They are represented in YAML format.  

[View a playbook file example here](https://github.com/nadmax/ansible101/blob/master/playbooks/example.yaml)