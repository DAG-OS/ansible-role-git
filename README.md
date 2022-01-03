# Ansible Role: Git

A role for installing and configuring Git.

## Requirements

In order to install Git, root privileges are required.

## Role Variables

* `state`: Defines the state this role aims to achieve, defaults to `present`.
  Available choices:
  * `present`: Install and configure Git.
  * `install`: Install Git.
  * `configure`: Configure Git.
* `git_settings`: A list of settings to set globally, e.g., `core.editor: vim`.
  See [Git docs](https://git-scm.com/docs/git-config#_variables) for a documented list of available values.

## Dependencies

None.

## Example Playbook

```yaml
- name: Install and configure Git
  hosts: all
  roles:
    - role: git
      vars:
        state: present
        git_settings:
          user.name: Max Mustermann
          user.email: max.mustermann@gmx.de
```

## License

MIT

## Author Information

This role was created in 2022 by Lucas Resch.
