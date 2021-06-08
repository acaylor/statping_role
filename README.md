Statping Role
=========

This will install and configure docker and a few containers to run statping.

Role Variables
--------------

- statping_db
- statping_host
- admin_email

Dependencies
------------

- geerlingguy.firewall
- geerlingguy.docker
- geerlingguy.pip
- community.docker

Pull dependencies with ansible-galaxy:
`ansible-galaxy install -r meta/requirements.yml`

Example Playbook
----------------

```yaml
---
- hosts: all
  become: yes
  vars:
    statping_db: "password"
    statping_host: "hostname.example.com"
    admin_email: "email@example.com"
    pip_install_packages:
      - name: docker
  roles:
    - statping_role
```

License
-------

BSD

Author Information
------------------

acaylor
