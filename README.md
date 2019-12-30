Role Name
=========

users

[![Build Status](https://travis-ci.org/cmihai-ansible/users.svg?branch=master)](https://travis-ci.org/cmihai-ansible/users)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/users](https://galaxy.ansible.com/crivetimihai/users)

```bash
ansible-galaxy install crivetimihai.users
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
users_remove_packages: true
users_enable_service: true
users_enable_selinux: true
users_firewall_configure: true
users_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install users on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: users is configured
      import_role:
        name: crivetimihai.users
      vars:
        users_remove_packages: true
        users_enable_service: true
        users_firewall_configure: true
        users_firewall_rules:
          - service:
      tags: users
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
