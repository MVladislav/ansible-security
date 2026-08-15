# Contributing

Thanks for your interest in contributing to `ansible-security`.

## Development setup

Install the development tooling (Ansible, linting, molecule) in a virtual
environment:

```sh
python3 -m venv .venv
source .venv/bin/activate
python3 -m pip install -r requirements.txt
```

Install pre-commit hooks (used by CI and recommended for local work):

```sh
python3 -m pip install pre-commit
pre-commit install
pre-commit run --all-files
```

## Making changes

1. Create a feature branch from `main`.
2. Make your changes following the existing conventions:
   - all role variables are prefixed with `security_` (except the legacy
     `clients` list);
   - Ubuntu only; use `apt` for packages and `systemd_service` for services;
   - tag every task with `security` plus the service name;
   - keep tasks idempotent and prefer modules over `command`/`shell`.
3. Run the checks locally:
   ```sh
   pre-commit run --all-files
   ```
4. Test against the supported platforms:
   ```sh
   molecule test -s ubuntu2404
   molecule test -s ubuntu2604
   ```
   (requires Docker; systemd-enabled Ubuntu 24.04 and 26.04 images are used)
5. Open a pull request against `main` and describe what changed and why.

## Commit messages

Use [conventional commits](https://www.conventionalcommits.org/), e.g.
`fix: ...`, `feat: ...`, `chore(deps): ...`, matching the repository history.
