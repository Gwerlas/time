Development guide
=================

Requirements
------------

Install and configure :

* libvirt
* vagrant
* vagrant-libvirt plugin
* molecule
* molecule-vagrant

Run tests
---------

Quick tests of the role without any options, ran in docker containers as `ansible` user :

```sh
molecule test
```

Test with custom NTP pool configured :

```sh
molecule test -s chrony
```

Develop / Debug
---------------

```sh
molecule create
molecule converge
molecule login -h <instance_name>
# Do your changes by hand
molecule verify
```

Submit your changes
-------------------

Merge request in Gitlab.
