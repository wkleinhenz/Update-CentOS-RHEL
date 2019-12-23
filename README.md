Update-CentOS-RHEL
===

Copyright (C) 2019 Dmitriy Prigoda <deamon.none@gmail.com> 
This script is free software: Everyone is permitted to copy and distribute verbatim copies of 
the GNU General Public License as published by the Free Software Foundation, either version 3
of the License, but changing it is not allowed.

For group update install CentOS/RHEL using Ansible
--------------------------------------------------

*Project structure: Update-CentOS-RHEL*

.
|___invetory
|   |
|   |___hosts
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
|___logs
    |
   	|___ansible-log.log
    
Playbooks|Effect
---------|------

