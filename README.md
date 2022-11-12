Time
====

[![pipeline status](https://gitlab.com/yoanncolin/ansible/roles/time/badges/main/pipeline.svg)](https://gitlab.com/yoanncolin/ansible/roles/time/-/commits/main)

Time synchronisation management.

GitLab project: [yoanncolin/ansible/roles/time](https://gitlab.com/yoanncolin/ansible/roles/time)

Requirements
------------

This role as been writen to be run as non root user, so Sudo has to be installed and configured.

The package manager has to be configured and the database of packages has to be populated.

Facts
-----

The `time_service` give You the name of the time service if You need to manage it later.

Tags
----

None.

Variables
---------

See [defaults/main.yml](defaults/main.yml).

Look at the distributions specific values in `vars/` directory.

Dependencies
------------

None.

Example Playbook
----------------

Common usage :

```yaml
---
- name: My wonderful playbook
  hosts: all
  roles:
    - name: gwerlas.time
```

With the legacy `ntp` package, and a list of custom NTP servers :

```yaml
---
- name: My wonderful playbook
  hosts: all
  roles:
    - name: gwerlas.time
      vars:
        time_backend_name: ntp
        time_servers:
          - 0.fr.pool.ntp.org
          - 1.fr.pool.ntp.org
          - 2.fr.pool.ntp.org
          - 3.fr.pool.ntp.org
```

License
-------

[BSD 3-Clause License](LICENSE).
