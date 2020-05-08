# Ansible Collection - ericsysmin.kubernetes

Ansible collection that holds roles, that can be used to configure common kubernetes services.

## Roles

| Role    | Build Status                                                                                                                                                                                                                                                                      | Documentation                                                                                            |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| kubectl | [![Role: ericsysmin.kubernetes.kubectl](https://github.com/ericsysmin/ansible-collection-kubernetes/workflows/ericsysmin.kubernetes.kubectl/badge.svg)](https://github.com/ericsysmin/ansible-collection-kubernetes/actions?query=workflow%3A%22ericsysmin.kubernetes.kubectl%22) | [Documentation](https://github.com/ericsysmin/ansible-collection-kubernetes/blob/master/docs/kubectl.md) |
| kompose | [![Role: ericsysmin.kubernetes.kompose](https://github.com/ericsysmin/ansible-collection-kubernetes/workflows/ericsysmin.kubernetes.kompose/badge.svg)](https://github.com/ericsysmin/ansible-collection-kubernetes/actions?query=workflow%3A%22ericsysmin.kubernetes.kompose%22) | [Documentation](https://github.com/ericsysmin/ansible-collection-kubernetes/blob/master/docs/kompose.md) |

## Usage

You can find specific to each role within the "Documentation" link for each role. However, most should be in this format.

```yaml
---
- hosts: localhost
  connection: local
  tasks:
    - name: Include role
      include_role:
        name: ericsysmin.kubernetes.<role_name>
      vars:
        var1: value1
        var2: value2
```

## Testing

Testing is done through GitHub Actions, and can be tested locally as well. GitHub Actions can be located [here](https://github.com/ericsysmin/ansible-collection-kubernetes/actions).
Each workflow pertains to a single role, and can be launched locally using the following command:

```bash
MOLECULE_COMMAND={{ matrix.molecule_distro.command }} \
MOLECULE_DISTRO={{ matrix.molecule_distro.distro }} \
molecule --debug test -s {{ matrix.collection_role }}
```

To decide on the `MOLECULE_COMMAND` value please refer to the `.github/workflow/{{ collection_role }}.yml` file as it will have the value for proper kubernetesd services.
