# Nginx deployment with Automated certbot SSL generation using Ansible Playbooks.
You have to clone this project on your host machine once Ansible has been installed.
Your target project is accessible here:

https://github.com/siavashfazli/simple-docker-app

# Docker installation on the target server
I have Automated Docker installation. with the ```install_docker.yml``` playbook you can easily install docker.
However, if you have any problem with the playbook use the official docker document.

https://docs.docker.com/engine/install/


# Project Docker images
Note 1: I strongly recommend to **Don't** use **latest** version. choose your desired version to prevent any conflict and unpredicted situations.

Note 2: If you encountered any restriction or sanction during pulling images, replace these addresses in the ```dns.yml``` file or use local docker registries.

 * 178.22.122.100
 * 10.202.10.202
 * 78.157.42.100

Also, these are images that I used for my project:

https://hub.docker.com/_/nginx

https://hub.docker.com/r/certbot/certbot

# Start Container
Simply just run ```start_container.yml```. just check **Dockerfile** to ensure everything is ok.


# Generate SSL
This step is a little bit tricky. In ```certbot.yml```, the first task is generating certificates then the SSL block is added to the main conf file. fill in your email and domain and once check the whole task. 
