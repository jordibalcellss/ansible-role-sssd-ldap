# ansible-role-sssd-ldap

An Ansible role to install and configure [SSSD](https://sssd.io/) against LDAP.

## Description

Usage scope takes into account a custom CA certificate and a LDAP directory.
Additionally, it adds a file in to `/etc/sudoers.d` for allowing a group sudo
ability.

The playbook restarts the machine once finished. This can be overridden
changing `reboot` within `defaults` variables. It appeared to be necessary for
SSSD to properly start.

## Compatibility

Tested under CentOS 7 and AlmaLinux 8/9.

## Example playbook

```yaml
---
- hosts: host-server
  tasks:
  - import_role:
    name: ansible-role-sssd-ldap
```

## License

This project is licensed under the MIT license - see the LICENSE file for
details.
