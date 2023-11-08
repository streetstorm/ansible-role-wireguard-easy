ansible-role-wireguard
=========

Requirements
------------

```yaml
- src: https://github.com/streetstorm/ansible-role-docker
  scm: git
  name: ansible-role-docker
```

Role Variables
--------------

```bash
wireguard_user: "wireguard"
wireguard_path: "/opt/wireguard"

wireguard_docker_name: "wireguard"
wireguard_image_name: "linuxserver/wireguard:v1.0.20210914-ls55"
wireguard_port: 51820
wireguard_proto: 'udp'

wireguard_server_url: 'auto'
wireguard_tz: 'Europe/Moscow'
wireguard_internal_subnet: "10.13.13.0"
wireguard_allowedips: "0.0.0.0/0" # example '10.13.13.2,192.168.1.0/24,192.168.2.0/24'
wireguard_logs_conf: true
wireguard_peers: 3
wireguard_peer_dns: 'auto'
wireguard_container_restart: 'unless-stopped'

wireguard_dir_state: 'directory'
wireguard_container_state: 'present'
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: ansible-role-wireguard, x: 42 }

License
-------

BSD

Author Information
------------------

@streetstorm
