# Insync

This role handles configuring the Insync repository and then install Insync.

## Requirements

The hosts you are targeting should have the following packages:

- python >= 2.6
- python-dnf

## Role Variables

None

## Dependencies

None

## Example Playbook


```yaml
- hosts: servers
  roles:
    - role: jaredhocutt.insync
```

## License
-------

MIT

## Author Information
------------------

Jared Hocutt (@jaredhocutt)
