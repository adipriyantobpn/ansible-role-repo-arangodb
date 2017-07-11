Ansible Role: ArangoDB Repository
=========

An Ansible Role that to manage ArangoDB Yum repository

Requirements
------------

This role needs no special requirements, except sudo access

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):


```yaml
---
repo_location:              international   # available options: international, vagrant
arangodb_enabled:            yes
arangodb_version:            3.4
```

Dependencies
------------

None

Example Playbook
----------------

We can use this roles multiple times with different `arangodb_version` like this:

```yaml
---
- name: Prepare CentOS 7 server
  hosts: centos7
  roles:
    - role: adipriyantobpn.repo-arangodb
      repo_location:              vagrant
      arangodb_enabled:           yes
      arangodb_version:           3.1
    - role: adipriyantobpn.repo-arangodb
      repo_location:              international
      arangodb_enabled:           no
      arangodb_version:           3
    - role: adipriyantobpn.repo-arangodb
      repo_location:              international
      arangodb_enabled:           no
      arangodb_version:           2
```

License
-------

BSD

Author Information
------------------

This role was created in 2017 by [Adi Priyanto](https://github.com/adipriyantobpn) as a learning purpose for community.