valheim-server
=========

installs and runs [valheim](https://www.valheimgame.com/)

Requirements
  debian or redhat systems 32 bit
  pending 64 bit support


Role Variables
--------------

| Variable | Description | Default |
|----------|-------------|---------|
| `gm_name` | username on host that owns server files and processes | `hvadmin` |

Dependencies
------------
roles:
  - src: https://github.com/aversiste/ansible-steamcmd.git
    name: aversiste.steamcmd
    version: master.

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
