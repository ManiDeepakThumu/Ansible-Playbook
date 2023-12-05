# Ansible Playbook for Nginx Docker Container
This Ansible playbook is designed to set up an Nginx Docker container on an Ubuntu 22.04 EC2 instance.

## Requirements
- Ansible installed on your local machine.
- An Ubuntu 22.04 EC2 instance.
- Docker registry credentials (username and password).

## Usage
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/ManiDeepakThumu/Ansible-Playbook.git

2. cd Ansible-Playbook

3. Edit the inventory.yml file to specify EC2 instance IP or hostname.

4. Create a vars.yml file and define the following variables:
   docker_registry_username: your_docker_username
   docker_registry_password: your_docker_password

5. Run the Ansible playbook:
   ansible-playbook -i inventory.yml -e @vars.yml nginx-docker.yml
   The playbook will prompt you for the Docker registry username and password.

6. Access Nginx: Open a web browser and navigate to https://your-ec2-instance-public-ip (replace with your actual EC2 
   instance IP).

Notes:
Make sure your EC2 instance is reachable from your local machine.
Ensure that Docker registry credentials are correct.
