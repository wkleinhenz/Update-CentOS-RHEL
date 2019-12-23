Update-CentOS-RHEL
===

Copyright (C) 2019 Dmitriy Prigoda <deamon.none@gmail.com> 
This script is free software: Everyone is permitted to copy and distribute verbatim copies of 
the GNU General Public License as published by the Free Software Foundation, either version 3
of the License, but changing it is not allowed.

For group update install CentOS/RHEL using Ansible
--------------------------------------------------

Requirements: (localhost)

- Ansible >= 2.4.2.0

*Project structure: Update-CentOS-RHEL*

    .
    ├── invetor
    |   |___hosts
    |   |
    |   |___hosts.example
    |
    |___playbooks
    |   |
    |   |___pre-config-ssh.yml
    |   |
    |   |___update-centos-rhel.yml
    |
    |___roles
    |   |
    |   |___update
    |   |  |
    |   |  |___tasks
    |   |      |
    |   |      |___main.yml
    |   |
    |   |___reboot
    |      |
    |      |___tasks
    |          |
    |          |___main.yml
    |
    |___files
    |   |
    |   |___keyfile
    |
    |___ansible.cfg
    |
    |___logs
        |
   	    |___ansible-log.log
        
## Create an Ansible Inventory
Create an inventory file with the appropriate groups and variables defined.
An example inventory can be found in [inventory/hosts.example](inventory/hosts.example).

## Run playbook:

```bash
cd Update-CentOS-RHEL
ansible-playbook -i inventory/hosts playbooks/pre-config-ssh.yml
ansible-playbook -i inventory/hosts playbooks/update-centos-rhel.yml
```

Playbooks|Effect
---------|------
pre-config-ssh.yml|Prepares the node, copies the SSH key
update-centos-rhel.yml|Installs the update and reboots the node

Use Ansible
===========
You can install a released version of Ansible via ``pip``, a package manager, or our `release repository <https://releases.ansible.com/ansible/>`_. See our `installation guide <https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html>`_ for details on installing Ansible on a variety of platforms.

## Documentation:
- [Ansible Documentations](https://docs.ansible.com/)
