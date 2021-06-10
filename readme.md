Ansible Caddy Installation Role
===============================

Install Caddy role.

## Role Variables

- `caddy_installation_packages`: The additional packages that should be included in the Caddy installation. (The packages can be found here: https://caddyserver.com/download)

## Example Playbook

```yaml
- hosts: all
  roles:
    - role: ansible-caddy-installation
      vars:
        caddy_installation_packages:
          - github.com/caddy-dns/digitalocean
```


## Versioning

In order to have a verioning in place and working, create leightweight tags that point to the appropriate minor release versions.

Creating a new minor release:

```bash
git tag 1.0
git push --tags
```

Replacing an already existing minor release:

```bash
git tag -d 1.0
git push origin :refs/tags/1.0
git tag 1.0
git push --tags
```
