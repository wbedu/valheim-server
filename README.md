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
| `gm_pass` | password for linux user (password is disabled as default)| not defined |
| `gm_ssh_key` | ssh public key (accepts url, lists, string, and lookup)| not defined |
| `run_valheim` | determins whether to run the game server or not | `yes` |
| `valheim_server_name` | default server name | `valheim community server` |
| `valheim_server_password` | default server password | `hunter2345` |
| `valheim_server_port` | default server port | `2456` |

Requirements
-----------

```yaml
roles:
  - src: https://github.com/Aversiste/ansible-steamcmd.git
    name: Aversiste.ansible-steamcmd
    version: master

```
Example Playbooks
----------------

#### Minimal example
```yaml
    - hosts: servers
      roles:
        - role: valheim-server
```

#### Full example
```yaml
    - hosts: servers
      roles:
        - role: valheim-server
          vars:
            gm_name: "user1234"
            gm_pass: "good secure password that won't be shared with non admins"
            gm_ssh_key: "{{ lookup('file', '~.ssh/id_rsa.pub') }}"
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
