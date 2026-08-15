# Description

Please include a summary of the changes and the issue they address, plus the
motivation and any dependencies required for the change.

Fixes # (issue)

## Type of change

- [ ] Bug fix (non-breaking change that fixes an issue)
- [ ] New feature (non-breaking change that adds functionality)
- [ ] Breaking change (fix or feature that changes existing behavior)
- [ ] Documentation update

## How has this been tested?

Please describe the tests you ran and how to reproduce them (molecule
scenarios, ad-hoc playbook, `--check` run).

- [ ] `molecule test -s ubuntu2404`
- [ ] `molecule test -s ubuntu2604`
- [ ] `pre-commit run --all-files`

## Checklist:

- [ ] My changes follow the project conventions (see `CONTRIBUTING.md`)
- [ ] All variables are prefixed with `security_` (legacy `clients` list excepted)
- [ ] Tasks are tagged with `security` and the service name
- [ ] `ansible-lint` and `yamllint` report no errors
- [ ] Molecule `verify.yml` assertions pass for the affected scenario(s)
- [ ] Documentation (README, templates) is updated where needed
- [ ] Commit messages follow [conventional commits](https://www.conventionalcommits.org/)
