# Server-Playbook
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
## Description
Ansible script to manage servers.

## Roles
The system use the following role namings:

| role prefix | meaning|
|---|---|
|system-|general system roles which apply basic configurations|
|native-|applications which run native on the system|
|docker-|applications which run on docker containers on the system|

## Update
Follow the best [practices for inventories](https://docs.ansible.com/ansible/2.3/playbooks_best_practices.html) and execute ansible via:

``bash
ansible-playbook -i ~/your-inventories/inventorie/hosts site.yml
``

## Debug
### Cleanup docker
``bash
docker stop $(docker ps -aq); docker rm $(docker ps -aq); docker volume rm $(docker volume ls -q);
``

## See
- https://wiki.archlinux.org/index.php/Ansible
