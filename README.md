# Ansible Role: hosts

[![Build Status](https://img.shields.io/travis/arillso/ansible.hosts.svg?branch=master&style=popout-square)](https://travis-ci.org/arillso/ansible.hosts) [![license](https://img.shields.io/github/license/mashape/apistatus.svg?style=popout-square)](https://sbaerlo.ch/licence) [![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-hosts-blue.svg?style=popout-square)](https://galaxy.ansible.com/arillso/hosts) [![Ansible Role](https://img.shields.io/ansible/role/d/24841.svg?style=popout-square)](https://galaxy.ansible.com/arillso/hosts)

## Description

Ansible role that dynamically creates the hosts file.

## Installation

```bash
ansible-galaxy install arillso.hosts
```

## Requirements

None

## Role Variables

### Loppback

Creates a 172.0.0.1 entry for the server name.

```yml
hosts_hostname_loopback: true
```

### Inventory

Inserts all hosts in the Ansible Inventory file into the Hosts file.

```yml
hosts_inventory_to_hosts: false
```

For `hosts_inventory_to_hosts` to work, the variable `internel_ansible_host` must be set in the `host_vars`, alternative can also be set to `ansible_host`.
Optionally, `hosts_aliases` can be set in the `host_vars`, then it generates aliases for the hosts.

### IPv6

Ipv6 localhost entries are set automatically. Setting false it can be prevented.

```yml
hosts_ipv6: true
```

## Dependencies

None

## Example Playbook

```yml
- hosts: all
  roles:
    - arillso.hosts
```

## Author

- [Simon Bärlocher](https://sbaerlocher.ch)

## License

This project is under the MIT License. See the [LICENSE](https://sbaerlo.ch/licence) file for the full license text.

## Copyright

(c) 2019, Arillso
