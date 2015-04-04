Nginx-Proxy
=========

Installs an nginx proxy site.

Requirements
------------

N/A

Role Variables
--------------

nginx_proxy_name: name for the configuration file, logs
nginx_proxy_listen: nginx port to listen on
nginx_proxy_server_name: nginx host to listen on
nginx_proxy_pass: proxy uri (eg. http://localhost:8080, or file://tmp/project.sock)


Dependencies
------------

geerlingguy.nginx

Example Playbook
----------------

Here is an example playbook for setting up a Gogs (http://gogs.io) nginx proxy.

    - hosts: Gogs server
      roles:
         - role: mnn.nginx-proxy
           nginx_proxy_name: gogs
           nginx_proxy_server_name: git.*
           nginx_proxy_pass: http://localhost:3000

License
-------

GPLv3

Author Information
------------------

This role was written by Justin Caratzas <bigjust@lambdaphil.es> for Mother Nature Network (https://github.com/MotherNatureNetwork)
