# ansible-roles-httpd

A simple Ansible role to install and configure the **Apache HTTPD** web server on RHEL/CentOS-based systems.

## Structure

```
.
├── ansible.cfg
├── inventory
├── playbook.yml
└── roles/
    └── httpd/
```

## Usage

### 1. Update inventory

Edit the `inventory` file to set your target hosts under the `[Dev]` group.

### 2. Run the playbook

```bash
ansible-playbook playbook.yml
```

## Requirements

- Ansible 2.9+
- Target hosts: RHEL / CentOS (systemd-based)
- SSH access with sudo privileges

## What it does

- Installs `httpd` via `yum`
- Starts and enables the `httpd` service
- Optionally manages firewall rules for port 80/443
