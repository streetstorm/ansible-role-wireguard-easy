ansible-role-wireguard-easy
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
wireguard_user: "wg-easy"
wireguard_path: "/opt/wg-easy"

wireguard_docker_name: "wg-easy"
wireguard_image_name: "weejewel/wg-easy"
wireguard_port: 51820
wireguard_proto: 'udp'
wireguard_ui_port: 51821
wireguard_ui_proto: 'tcp'

wireguard_ui_password_lang: 'en'
wireguard_ui_password: '$2a$12$CCDAP/qVvR3XXdEsiwHpNeGKeQs.WVen/oggwCi8.y05M/lQWwdxW' # PasswordWG # Для генерации hash пароля: docker run -it ghcr.io/wg-easy/wg-easy wgpw PasswordWG
wireguard_server_url: '0.0.0.0'
wireguard_allowedips: "0.0.0.0/0" # example '10.13.13.2,192.168.1.0/24,192.168.2.0/24'
wireguard_keepalive_seconds: 0

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
         - { role: ansible-role-wireguard-easy, x: 42 }

License
-------

BSD

Author Information
------------------

@streetstorm
