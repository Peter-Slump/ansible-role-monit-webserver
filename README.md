# Ansible role Monit webserver

Version: 0.0.1

Supported OS: Ubuntu

Ansible role Monit webserver

## Role variables
```
monit_webserver_hostname: monit.example.com

# SSL settings passed to the Nginx role
monit_webserver_use_self_signed_ssl: False
monit_webserver_use_letsencrypt: False

# Webserver configurations
monit_webserver_http_port: 2812
monit_webserver_accept_from: 0.0.1.0
monit_webserver_allow_from: 0.0.1.0

# Credentials for the admin user
monit_webserver_username: admin
monit_webserver_password: super-secret-password
```

## Example
```
- hosts: all
  roles:
    - role: monit-webserver
      monit_webserver_password: "{{ vault_monit_webserver_password }}"
```
