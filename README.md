valheim-server
=========

installs and runs [valheim](https://www.valheimgame.com/)

Requirements
------------
```yaml
roles:
  - src: https://github.com/aversiste/ansible-steamcmd.git
    name: aversiste.steamcmd
    version: master

```

Role Variables
--------------

| Variable | Description | Default |
|----------|-------------|---------|
| `gm_name` | username on host that owns server files and processes | `hvadmin` |

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:
```yaml
    - hosts: servers
      roles:
         - { role: valheim-server, x: 42 }

    - hosts: servers
        roles:
          - { role: valheim-server, gm_name: "user1234" }
```
License
-------

MIT

Author Information
------------------
wbedu@github | me@willbedu.com
