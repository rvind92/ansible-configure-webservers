# ansible-configure-webservers

This Ansible playbook is used to install NGINX and to configure it as a reverse proxy with a sample upstream server (collectius-vm-2).

There are 2 VMs that already been configured and set up in Azure:
1. The first VM (collectius-vm-1) serves as a reverse proxy load balancer with NGINX.
2. The second VM (collectius-vm-2) serves as the web server.

To run this playbook:

1. Ensure Ansible is installed on your local machine. (see https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html)
2. Clone this repository to your local machine.
3. Change your directory to the clone repository.
4. In your terminal or command line, type in the following command: ansible-playbook -i inventory.ini nginx_reverse_proxy_setup.yml --ask-become-pass
5. Enter the password when prompted.

Once the playbook has completed executing, open your browser and visit the first VM's public IP at 20.168.78.23. You should see the landing page with the message: Welcome to collectius-vm-2!
