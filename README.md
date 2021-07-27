Nginx
=======

This playbook can be used on AWX or Tower
Install and configuring the Nginx and SSL on RHEL/CentOS, Debian 9,10 and Ubuntu 20.04

- Install the necessary packages;
- Configure nginx, vhost and ssl.

Requirements
------------

- The SELinux and firewall settings are not considered to be a concern of this role.

Role Variables
--------------

Necessary changes to defaults/main.yml

| Variables                                    | Defaults                      | Comments
| :---                                         | :---                          | :---                                                    
| `nginx_AWX_TOWER_domain`                     |                               | Inform your domain
|                                              |                               |

Variables that can be changed if you want.
For Red Hat family:

| Variables                                    | Defaults                     |
|:---                                          |:---                          |:---
| `nginx_AWX_TOWER_log_path`                   | /var/log/nginx/              |
|                                              |                              |
| `nginx_AWX_TOWER_ssl_path`                   | /etc/nginx/ssl-certs/        |
|                                              |                              |
| `nginx_AWX_TOWER_vhost_path`                 | /etc/nginx/conf.d/           |
|                                              |                              |
| `nginx_AWX_TOWER_repo`                       |                              | Nginx repository for RedHat/CentOS 7
|                                              |                              |

Variables that can be changed if you want.
For Debian family:

| Variables                                    | Defaults
|:---                                          |:---
| `nginx_AWX_TOWER_log_path`                   | /var/log/nginx/
|                                              |
| `nginx_AWX_TOWER_ssl_path`                   | /etc/nginx/ssl-certs/
|                                              |
| `nginx_AWX_TOWER_vhost_path`                 | /etc/nginx/conf.d/
|                                              |

Dependencies
------------

No dependencies.

Installing Certificates
-----------------------

It is necessary to exchange the certificates below for your certificates

```
├── files
│   ├── almircandido.com.crt
│   └── almircandido.com.key

```

## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section.


Author Information
------------------
LinkedIn: https://br.linkedin.com/in/almircandido/
