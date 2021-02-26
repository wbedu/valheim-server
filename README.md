valheim-server
=========

installs and runs [valheim](https://www.valheimgame.com/)

Requirements
------------

  debian OS Family

Role Variables
--------------

| Variable | Description | Default |
|----------|-------------|---------|
| `gm_name` | username on host that owns server files and processes | `hvadmin` |
| `gm_pass` | password for linux user |  not defined|
| `run_valheim` | determins whether to run the game server or not | `yes` |
| `valheim_server_name` | valheim server name | `valheim community server` |
| `valheim_server_password` | valheim server password | `hunter2345` |
| `valheim_server_port` | valheim server port | `2456` |

```yaml
roles:
  - src: https://github.com/Aversiste/ansible-steamcmd.git
    name: Aversiste.ansible-steamcmd
    version: master

```
Example Playbooks
----------------

```yaml
    - hosts: servers
      roles:
        - { role: valheim-server, gm_name: "user1234" }
```


```yaml
    - hosts: servers
      roles:
        - role: valheim-server
          vars:
            gm_name: "user1234"
            gm_pass: "good secure password that won't be shared with non admins"
            run_valheim: yes
            valheim_server_name: "server 0123"
            valheim_server_password: "sooper dooper secret"
            valheim_server_port: "2456"
```
License
-------

MIT

Author Information
------------------
wbedu@github | me@willbedu.com
