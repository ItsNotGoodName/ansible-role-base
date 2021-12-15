# ansible-role-base

A role that setups a base Linux system.

- Update system using the `base_update` tag
- Install and configure packages
- Optionally Set hostname and timezone
- Create groups and users

## Requirements

N/A

## Role Variables

`base_hostname` sets the server's hostname.

`base_timezone` sets the server's timezone (e.g. `America/Los_Angeles`).

## Dependencies

N/A

## Example Playbook

```yaml
- hosts: all
  roles:
    - itsnotgoodname.base
```

## License

MIT

## Author Information

ItsNotGoodName
