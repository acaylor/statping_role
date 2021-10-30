Statping Role
=========

This will install and configure docker and a few containers to run statping.

Role Variables
--------------

- statping_db: postgres password
- statping_host: internet facing hostname
- admin_email: email to provide to let's encrypt (free SSL/TLS certificates)

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

Supported platforms
--------------------

- Ubuntu 20.04 LTS x86_64

License
-------

BSD

Author Information
------------------

acaylor
