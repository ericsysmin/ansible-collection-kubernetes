# ericsysmin.kubernetes.kubectl

[![ericsysmin.kubernetes.kubectl](https://github.com/ericsysmin/ansible-collection-kubernetes/actions/workflows/kubectl.yml/badge.svg)](https://github.com/ericsysmin/ansible-collection-kubernetes/actions/workflows/kubectl.yml)

A brief description of the role goes here.

## Requirements

None

## Role Variables

| Variable          | Required | Default | Comments                           |
| ----------------- | -------- | ------- | ---------------------------------- |
| `kubectl_version` | No       | `1.29`  | Version of kubectl to be installed |

## Dependencies

None

## Example Playbook

```yaml
- hosts: servers
    roles:
      - role: ericsysmin.kubectl
        kubectl_version: 1.29
```

## License

MIT

## Author Information

[ericsysmin](https://ericsysmin.com)
