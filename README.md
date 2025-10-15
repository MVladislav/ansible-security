# Security

[![Ansible Lint](https://github.com/MVladislav/ansible-security/actions/workflows/ansible-lint.yml/badge.svg)](https://github.com/MVladislav/ansible-security/actions/workflows/ansible-lint.yml)
[![Ansible Molecule Test](https://github.com/MVladislav/ansible-security/actions/workflows/ci.yml/badge.svg)](https://github.com/MVladislav/ansible-security/actions/workflows/ci.yml)

- [Security](#security)
  - [Role Variables](#role-variables)
  - [Dependencies](#dependencies)
  - [Example Playbook](#example-playbook)
  - [License](#license)

---

You can checkout [MVladislav - ansible-env-setup - playbooks](https://github.com/MVladislav/ansible-env-setup/tree/main/playbooks) for how i use it in general.

Tested with:

- Ubuntu 23.04
- Ubuntu 24.04
- Ubuntu 25.04

## Role Variables

```yml
security_setup_services:
  auditd: true
  fail2ban: true
  snmp: false
  ssh: true

clients:
  - name: "{{ ansible_user }}"

security_fail2ban_proxmox: false

security_snmp_user: snmp
security_snmp_password: <PASSWORD>
security_snmp_encryption: <ENC>
security_snmp_location: home
security_snmp_contact: root
security_snmp_address_ipv4: "{{ omit }}"
security_snmp_address_ipv6: "{{ omit }}"
security_snmp_port_ipv4: 161
# security_snmp_port_ipv6: 161
```

## Dependencies

Developed and testes with Ansible 2.14.4

## Example Playbook

```yml
- hosts: servers
  roles:
    - role: security
      ansible_user: <TODO-USERNAME>

      security_setup_services:
        auditd: true
        fail2ban: true
        snmp: false
        ssh: true

      clients:
        - name: "{{ ansible_user }}"

      security_fail2ban_proxmox: false

      security_snmp_user: snmp
      security_snmp_password: <PASSWORD>
      security_snmp_encryption: <ENC>
      security_snmp_location: home
      security_snmp_contact: root
      security_snmp_address_ipv4: "{{ omit }}"
      security_snmp_address_ipv6: "{{ omit }}"
      security_snmp_port_ipv4: 161
      # security_snmp_port_ipv6: 161
```

## License

MIT
