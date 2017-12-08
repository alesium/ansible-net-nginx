[![Build Status](https://travis-ci.org/alesium/ansible-net-nginx.svg?branch=master)](https://travis-ci.org/alesium/ansible-net-nginx)

net-nginx
=========

Ansible Role to configure nginx from pkgsrc

Requirements
------------

- Hosts requires pkgsrc's pkgin
- Hosts should be bootstrapped for ansible usage (have python,...)
- Root privileges, eg `become: yes`

Role Variables
--------------

| Variable | Description | Default value |
|----------|-------------|---------------|
| `net_nginx_service_name` | Service name for handler | `"pkgsrc/nginx"` | 
| `net_nginx_config_file_src` | nginx.cfg.j2 source file location | `"nginx.cfg.j2"` | 
| `net_nginx_config_file_dest` | nginx.cfg.j2 remote location | `"/opt/local/etc/nginx.cfg"` | 

Dependencies
------------

None

Example Playbook
----------------


    - hosts: servers
      roles:
         - { role: alesium.net-nginx }

License
-------

BSD

Author Information
------------------

Sebastien Perreault <sperreault@alesium.net>
