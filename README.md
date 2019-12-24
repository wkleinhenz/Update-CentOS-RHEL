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
    ├── inventory
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

This project is hosted at:

  * https://github.com/D34m0nN0n3/Update-CentOS-RHEL/

For the latest version, to contribute, and for more information, please visit
the project pages.

To clone the current master branch run:

```
git clone https://github.com/D34m0nN0n3/Update-CentOS-RHEL.git
```

## Create an Ansible Inventory
Create an inventory file with the appropriate groups and variables defined.
An example inventory can be found in [inventory/hosts.example](inventory/hosts.example).

## Run playbook:

```bash
cd Update-CentOS-RHEL
ansible-playbook -i inventory/hosts playbooks/pre-config-ssh.yml --ask-pass
ansible-playbook -i inventory/hosts playbooks/update-centos-rhel.yml
```

Playbooks|Effect
---------|------
pre-config-ssh.yml|Prepares the node, copies the SSH key
update-centos-rhel.yml|Installs the update and reboots the node

## Documentation:
- [Ansible installation guide](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [Ansible Documentations](https://docs.ansible.com/)
