# ansible-mongodb-example

Example of MongoDB provisioning using Ansible.

## Note

This repository uses a pre existing Ansible role developed by UnderGreen user located in:
[ansible-role-mongodb](https://github.com/UnderGreen/ansible-role-mongodb).

A git submodule is included in this repository. All credit goes to its author/authors.

## Note 2

As mentioned in UnderGreen's repository, in order to use this role in prodution, several variables must be changed.
In addition, ansible vault or vault storing mechanism should be used for sensitive data.

## Launch playbook against a Vagrant machine

Note: in Vagrantfile, Amazon Linux 2 is used.

### Init Vagrantfile

This step isn't needed as Vagrantfile is included in this repository

```bash
vagrant init gbailey/amzn2
```

### Start Vagrant box

```bash
vagrant up
```

## Launch ansible playbook

```bash
ansible-playbook -i inventories/inventory.ini playbooks/mongodb.yml
```

## SSH into the box

```bash
vagrant ssh
```

### To destroy the box

```bash
vagrant destroy
```
