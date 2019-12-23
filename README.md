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

## Documentation:
[Ansible](https://docs.ansible.com/)
