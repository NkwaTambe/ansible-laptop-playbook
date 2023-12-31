# GIS Ansible Playbook

This playbook is used to install and configure a GIS laptops.

## Requirements
- python3
- ansible

## Usage
```bash
ansible-playbook -i hosts.ini gis/laptop/site.yml --connection=local -e "nvm=true" -e "sdkman=true"
```