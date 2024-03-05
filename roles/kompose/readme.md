# ericsysmin.kubernetes.kompose

[![ericsysmin.kubernetes.kompose](https://github.com/ericsysmin/ansible-collection-kubernetes/actions/workflows/kompose.yml/badge.svg)](https://github.com/ericsysmin/ansible-collection-kubernetes/actions/workflows/kompose.yml)

This role installs kompose on linux systems.

## Requirements

None

## Role Variables

| Variable          | Required | Default  | Comments                           |
| ----------------- | -------- | -------- | ---------------------------------- |
| `kompose_version` | No       | `1.32.0` | Version of Kompose to be installed |

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
  roles:
    - role: ericsysmin.kompose
      kompose_version: 1.17.0
```

## License

MIT

## Author Information

[ericsysmin](https://ericsysmin.com)
