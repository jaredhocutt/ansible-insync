# Insync

This role handles configuring the Insync repository and then install Insync.

## Requirements

The hosts you are targeting should have the following packages:

- python >= 2.6
- python-dnf

## Role Variables


| Variable          | Required | Default       | Description                                                                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | -------- | ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| insync_releasever | &#9989;  | `$releasever` | The `releasever` to use when creating the yum repository.<br><br>By default, this will use the `$releasever` of the OS, but Insync tends to be pretty behind on it's yum repository, so sometimes you need to hard code this to an older version (e.g. The latest Fedora repo provided by Insync is 29, so using `$releasever` for Fedora 30 doesn't work and needs to be hard coded to `29`. |

## Dependencies

None

## Example Playbook


```yaml
- hosts: servers
  roles:
    - role: jaredhocutt.insync
      vars:
        insync_releasever: 29
```

## License

MIT

## Author Information

Jared Hocutt (@jaredhocutt)
