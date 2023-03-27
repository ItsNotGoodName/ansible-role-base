# ansible-role-base

Setup a base Linux/OpenBSD system.

- Install and configure packages
- Update packages using the `base_update` tag
- Set hostname and timezone
- Create groups and users
- Better default `tmux.conf`
- Exclusive authorized ssh keys
- Vi mode for shell

# Requirements

N/A

# Role Variables

Example `base_users` variable.

```yaml
base_users:
  - name: test
    shell: /bin/bash
    groups: sudo
    authorized_keys_exclusive: true
    authorized_keys:
      - ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIMYweYtPrNih4Jq2AboikznNOO/lHyBtiq+UR/lX2gNp test@test
```

Example `base_groups` variable.

```yaml
base_groups:
  - name: test
```

You can have multiple `base_users` and `base_groups` by adding a suffix to them (e.g. `base_users_test`).
They will be merged into `base_users` and `base_groups` respectively.

## Optional

`base_hostname` sets the server's hostname.

`base_timezone` sets the server's timezone (e.g. `America/Los_Angeles`).

# Dependencies

N/A

# Example Playbook

```yaml
- hosts: all
  roles:
    - itsnotgoodname.base
```

# License

MIT

# Author Information

ItsNotGoodName
