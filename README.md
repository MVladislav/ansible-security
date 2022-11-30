# Role Name

**security**

[![Ansible Lint](https://github.com/MVladislav/ansible-security/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/MVladislav/ansible-security/actions/workflows/ansible-lint.yml)

## Requirements

_Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required._

## Role Variables

_A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well._

## Dependencies

_A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles._

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: servers
  roles:
    - role: security
      security_setup_services:
        - auditd: true
        - fail2ban: true

      security_jail_bantime: 3600
      security_jail_banaction: iptables-multiport
      security_jail_enabled: true
      security_jail_maxretry: 3
      security_fail2ban_proxmox: false
```

## License

GNU AFFERO GENERAL PUBLIC LICENSE

## Author Information

MVladislav
