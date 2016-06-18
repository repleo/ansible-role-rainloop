Ansible role - rainloop webmail client installer
=====

[![Build Status](https://travis-ci.org/repleo/ansible-role-rainloop.svg?branch=master)](https://travis-ci.org/repleo/ansible-role-rainloop)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-repleo.rainloop-660198.svg?style=flat)](https://galaxy.ansible.com/repleo/rainloop)

This role install and configures rainloop. Rainloop is a modern webmail client.

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------

   # General config.
   rainloop_hostname: mail.example.com

   # SSL Configuration.
   rainloop_ssl: no
   rainloop_redirect_http_to_https: yes
   rainloop_ssl_certificate: "/etc/nginx/ssl/rainloop.crt"
   rainloop_ssl_certificate_key: "/etc/nginx/ssl/rainloop.key"

   # Database config.
   rainloop_db_user: rainloop
   rainloop_db_password: rainloop
   rainloop_db_host: localhost
   rainloop_db_name: rainloopdb


Dependencies
------------

- repleo.nginx
- repleo.postgresql

Example Playbook
----------------

Install rainloop
```yaml
- { role: repleo.rainloop,
     rainloop_hostname: berichten.repleo.nl,
     rainloop_ssl: yes,
     rainloop_ssl_certificate: /etc/nginx/ssl/ssl.repleo.nl-chain.pem,
     rainloop_ssl_certificate_key: /etc/nginx/ssl/ssl.repleo.nl.key
  }

```

License
-------

GPL v3 - (c) 2016, Repleo, Amstelveen

Author Information
------------------

Repleo, Amstelveen, Holland -- www.repleo.nl  
Jeroen Arnoldus (jeroen@repleo.nl)


