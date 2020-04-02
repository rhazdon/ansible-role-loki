Ansible Role Loki
=================

This role installs [Loki](https://github.com/grafana/loki/).

Loki is a horizontally-scalable, highly-available, multi-tenant log aggregation system inspired by Prometheus. It is designed to be very cost effective and easy to operate. It does not index the contents of the logs, but rather a set of labels for each log stream.

Requirements
------------
None.

But you should think about a reverse proxy like NGINX.

Role Variables
--------------

``` yaml
loki_version: "1.3.0"

# Installation from source settings
loki_install_from_source: false
loki_home_dir: /opt/loki
loki_config_dir: /etc/loki
loki_executable: /usr/local/bin/loki
loki_executable_options:
```

Dependencies
------------
None.

Example Playbook
----------------

``` yaml
- hosts: all
  roles:
    - { role: rhazdon.loki, tags: loki }
```

License
-------

MIT

Author Information
------------------

This role was created in 2020 by Djordje Atlialp.
