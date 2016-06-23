# Ansible Role: gem

This role will setup defined ruby gems.

## Requirements

- Ansible 1.9.6+

## Dependencies

None.

## Role Variables

| Name                | Default | Type  | Description       |
| ------------------- | ------- | ----  | ----------------- |
|    `gem_packages`   | [ ]     | Array | Ruby gems list    |

### Configuration example

```yaml
gem_packages:
  - name:          net-ssh
    version:       ~> 2.0
    user_install:  false
```
## Group Vars Example

    gem_packages           :

      - name:          test-kitchen
        version:       1.0.0
        user_install:  false

      - name:          kitchen-ansiblepush
        version:       4.0.0
        repository:    'https://github.com/msghaleb/kitchen-ansiblepush.git'
        user_install:  false

## Example playbook

    - hosts: servers
      roles:
         - { role: ansible-gem }

# Licence

MIT

# Author information

Mohamed Ghaleb
