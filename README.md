# vagrant-openwrt-ansible
This repository is a an example of usage of [Ansible Provisioner](https://www.vagrantup.com/docs/provisioning/ansible) with [Vagrant OpenWrt box](https://github.com/vladimir-babichev/vagrant-openwrt-box).

## Description
[`ansible-example` role](roles/ansible-example/tasks/main.yaml) will replace `wpad-mini` package with `wpad` one.

## Usage
Firstly install dependencies by running `make setup`. Then follow regular vagrant workflow:
- `vagrant up`
- `vagrant ssh`
- `vagrant destroy`

## Notes
This example is based on [ansible-openwrt role](https://github.com/gekmihesg/ansible-openwrt). For more information about the role, configuration or use scenarios, please refer to role's documentation.
