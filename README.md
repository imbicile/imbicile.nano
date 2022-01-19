# Role Name

imbicile.nano

## Example Playbook

```yml
- hosts:
    - all
  become: yes
  roles:
    - role: imbicile.nano
      tags: nano
```

## Author Information

https://imbicile.pp.ru

## Highlight in use

https://github.com/scopatz/nanorc

### previosly use

https://github.com/serialhex/nano-highlight

## ansible.cfg

```yml
[defaults]
deprecation_warnings=False
host_key_checking = False
roles_path = roles
interpreter_python=/usr/bin/python3
ansible_python_interpreter=/usr/bin/python3
force_valid_group_names = ignore
callback_whitelist = ansible.posix.profile_tasks

gathering = smart
fact_caching = jsonfile
fact_caching_connection = cache/facts
fact_caching_timeout = 3600

[inventory]
cache = yes
cache_plugin = jsonfile
cache_connection = cache/inventory
cache_timeout = 3600

[ssh_connection]
control_path = %(directory)s/%%C
retries = 2
```
