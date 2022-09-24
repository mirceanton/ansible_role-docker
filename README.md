Ansible Role: Docker
====================

An Ansible role that installs Docker.

Requirements
------------

N/A

Role Variables
--------------

|         Variable         |     Type     | Default |                 Description                 |
| :----------------------: | :----------: | :-----: | :-----------------------------------------: |
|      `docker_users`      | list(string) |  `[]`   | List of users to add to the `docker` group. |
| `docker_compose_install` |     bool     | `true`  | Whether or not to install `docker-compose`  |

To check the default variables, take a look at the [defaults](defaults/main.yml) file.

Dependencies
------------

N/A

Example Playbook
----------------

``` yml
---
- hosts: all
  remote_user: root

  roles:
    - role: mirceanton.docker
      vars:
        docker_users:
          - foo
          - bar
          - mike
```

License
-------

MIT

Author Information
------------------

A role developed by [Mircea-Pavel ANTON](https://www.mirceanton.com).
