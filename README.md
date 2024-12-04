# SurrealDB Cluster Deployment

This Ansible playbook deploys a production-ready SurrealDB cluster with TiKV backend.

## Prerequisites
- Ansible 2.9+
- Target servers running Ubuntu 20.04+
- SSH access to target servers

## Usage
1. Edit inventory.yml with your server IPs
2. Update group_vars/vault.yml with your passwords
3. Run: ansible-playbook -i inventory.yml site.yml --ask-vault-pass

## Structure
- group_vars/: Group variables
- roles/: Role-specific tasks and configurations
- templates/: Jinja2 templates
- site.yml: Main playbook
- inventory.yml: Inventory file

## Roles
- common: Basic system setup
- pd: Placement Driver setup
- tikv: TiKV store setup
- surrealdb: SurrealDB setup