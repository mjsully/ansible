# Ansible
Git repo to hold my Ansible playbooks. Very much a work in progress! Contains playbooks to provision new VMs, LXCs or Raspberry Pis, rollout Docker containers and perform general maintenance tasks.
## Basic setup
First, clone this repo. To install Ansible, use the following commands to ensure you have a valid Python3 install:
```
sudo apt update
sudo apt upgrade
sudo apt install python3-venv
sudo apt install python3-pip
```
Next, setup a venv within the ansible directory:
```
python3 -m venv ansible
cd ansible
```
## Running playbooks
To run a playbook, you can use the following command:
```
ansible-playbook -i inventories/sample.yaml (--limit sample) playbooks/maintenance/update_upgrade.yaml
```
This will run the 'update_upgrade.yaml' playbook on all hosts in the 'sample' group in the inventories/sample.yaml inventory. The optional `--limit <group>` command enables a playbook to be run on just one of the groups you have in your inventory, which is useful as your inventory grows.
