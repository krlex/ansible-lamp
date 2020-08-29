# ansible-certbot
Ansible certbot role

An Ansible role that generates new Let's Encrypt certificates

## Requirements

None

## Role Variables

- `certbot_enable` (boolean: true|false), default: `true`
- `certbot_webroot_remote_path` (string), default: `/var/www/letsencrypt/`
- `certbot_webroot_local_path` (string), default: `/tmp/letsencrypt-webroot-share/`
- `certbot_admin_email` (string), default: `email@example.com`
- `certbot_certs` (array) default: []
  ```

  ```

- `generated_certs_copy_to_local` (boolean: true|false), default: `false`
- `generated_certs_local_path` (string), default: `''`

## Dependencies

SSHFS installed locally.

## Example Playbook

    - hosts: servers
      vars:
        certbot_admin_email: 'admin@test.com'
        certbot_certs:
          - domains:
            - www.test.com
            - test.com
      roles:
         - { role: infloop.ansible-certbot }


## License
BSD
