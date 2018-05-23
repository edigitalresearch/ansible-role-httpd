# HTTPD role for ansible.

This is a Ansible role for configuring HTTPD


## Variables

Here is an example variables file

```
httpd:
  vhosts:
    - domain: example.com
      content: |
        <VirtualHost *:80>
            ServerName www.example.com
            ServerAlias example.com
            DocumentRoot /var/www/vhosts/example.com/
        </VirtualHost>
```

## Handlers

This role provides two handlers

* `start-httpd`
* `reload-httpd`

## Example Task with role

```
- name: manage httpd installation
  hosts: web
  roles:
    - edr.httpd
```
