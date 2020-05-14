WAL-G
=========

A role to install [wal-g][1] archival restoration tool.

Requirements
------------

Ansible control node requires [python-jmespath][2] to get latest release URL from github API.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```
walg_bin_path: /usr/local/bin
```

Installation path for `wal-g` (default: /usr/local/bin)

```
walg_owner: root
```

Owner of the `wal-g` binary.

```
walg_release_url: "https://api.github.com/repos/wal-g/wal-g/releases/latest"
```

API URL of wal-g github releases.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: islander.wal-g

If you need to modify installation path:

    - hosts: servers
      roles:
         - { role: islander.wal-g, walg_bin_path: /opt/bin }

License
-------

BSD

Author Information
------------------

This role was created by [kiba][3]

[1]: https://github.com/wal-g/wal-g
[2]: https://pypi.org/project/jmespath/
[3]: https://kiba.io
