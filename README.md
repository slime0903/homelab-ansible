# Ansible Homelab Automation

A hands-on infrastructure automation project using Ansible to manage Linux servers in a personal Proxmox homelab.

## Project Overview

This project demonstrates configuration management, Linux administration, SSH-based automation, and reusable Ansible roles.

An Arch Linux ThinkPad acts as the Ansible control node, managing an Ubuntu Server virtual machine hosted on Proxmox VE.

## Technologies

- Arch Linux — Ansible control node
- Ubuntu Server 24.04 — Managed Linux server
- Proxmox VE — Virtualization platform
- Ansible — Infrastructure automation
- OpenSSH — Secure remote administration
- Git and GitHub — Version control

## Current Features

- SSH key-based remote connectivity
- Automated Linux system information collection
- Package management with Ansible
- SSH service management using systemd
- Reusable Ansible roles
- Idempotent configuration management

## Project Structure

```text
homelab-ansible/
├── ansible.cfg
├── inventory/
│   ├── hosts.yml
│   └── group_vars/
├── playbooks/
│   ├── ubuntu-common.yml
│   ├── ubuntu-packages.yml
│   ├── ubuntu-setup.yml
│   ├── ubuntu-ssh.yml
│   └── ubuntu-system-info.yml
└── roles/
    ├── common/
    └── ssh/
```

## Running the Automation

Install Ansible on the control node and configure the inventory for your own managed servers.

Verify connectivity:

```bash
ansible linux_vms -m ping
```

Check playbook syntax:

```bash
ansible-playbook playbooks/ubuntu-setup.yml --syntax-check
```

Run the server configuration:

```bash
ansible-playbook playbooks/ubuntu-setup.yml --ask-become-pass
```

## Future Improvements

- Docker installation and service management
- Automated container deployment
- Additional Linux server configuration
- Monitoring and security automation
- Integration with a cybersecurity homelab

## Learning Objectives

This project is part of a practical learning portfolio focused on Linux administration, infrastructure automation, networking, and cybersecurity.
