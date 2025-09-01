Ansible Caddy Installation Role
===============================

Install Caddy role.

## Role Variables

- `caddy_installation_packages`: The additional packages that should be included in the Caddy installation. (The packages can be found here: https://caddyserver.com/download)

## Example Playbook

```yaml
- hosts: all
  tasks:
    - ansible.builtin.include_role:
        name: ansible-caddy-installation
      vars:
        caddy_installation_packages:
          - github.com/caddy-dns/digitalocean
```

## Build & Publish

To build and publish the role, visit the GitHub Actions page of the repository and trigger the workflow "Release Package" manually.
