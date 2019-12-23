Update-CentOS-RHEL
===

Copyright (C) 2019 Dmitriy Prigoda <deamon.none@gmail.com> 
This script is free software: Everyone is permitted to copy and distribute verbatim copies of 
the GNU General Public License as published by the Free Software Foundation, either version 3
of the License, but changing it is not allowed.

For group update install CentOS/RHEL using Ansible
--------------------------------------------------

*Project structure: Update-CentOS-RHEL*
|---invetory
|   |
|   |---hosts
|
|---playbooks
|   |
|   |---pre-config-ssh.yml
|   |
|   |---update-centos-rhel.yml
|
|---roles
|   |
|   |--update
|   |  |
|   |  |---tasks
|   |      |
|   |      |---main.yml
|   |
|   |--reboot
|      |
|      |---tasks
|          |
|          |---main.yml
|
|---files
|   |
|   |---keyfile
|
|---logs
    |
    |---ansible-log.log
    
    
