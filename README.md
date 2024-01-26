# Nginx deployment with Automated certbot SSL generation using Ansible Playbooks.
You have to clone this project on your host machine that Ansible has been installed.
Your target project is accessable here:

https://github.com/siavashfazli/simple-docker-app

In future I will automat docker installation with Ansible too, but currently we have to install it manually.

# Docker installation on target server
At first step you have to install Docker and related images on your target(Production) server. My suggestion is Docker official document:

https://docs.docker.com/engine/install/


# Project Docker images
Note 1 : I storngly recommend to **Don't** use **latest** version. choose your desired version to prevent any conflict and unpreidicted situations.
Note 2 : If you encountered with any restriction or sanction during pulling images, replace these addresses in ```dns.yml``` file.

 * 178.22.122.100
 * 10.202.10.202
 * 78.157.42.100
 * 
Also these are images that I used for my project:

https://hub.docker.com/_/nginx
https://hub.docker.com/r/certbot/certbot

Probably you have to run ```python_lib.yml``` playbook. because ansible requires ```docker``` and ```docker-compose``` libraries to execute container related commands.
