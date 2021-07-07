# Role Name

**security**, currently is hardening 4 defined definition from **_CIS Ubuntu Linux Benchmark_**

- 2.2.4 Ensure CUPS is not enabled ✓
- 6.1.2 Ensure permissions on /etc/passwd are configured ✓
- 1.3.3 Ensure sudo log file exists ✓
- 2.3.4 Ensure telnet client is not installed ✓

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
    - security
```

## License

GNU AFFERO GENERAL PUBLIC LICENSE

## Author Information

MVladislav
