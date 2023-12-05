# Ansible Playbook for Nginx Docker Container 
This Ansible playbook is designed to set up an Nginx Docker container on an Ubuntu 22.04 EC2 instance.

# Requirements 
*An Ubuntu 22.04 EC2 instance in running state.
Ensure Ansible is installed on EC2 instance.
Docker registry credentials (username and password).

# Running Playbook
Clone this repository to EC2 instance:
git clone https://github.com/ManiDeepakThumu/Ansible-Playbook.git

Navigate into the cloned directory by running this command:
cd Ansible-Playbook

Run the playbook to pull nginx image and spin container:
ansible-playbook nginx-docker.yml

Once the playbook starts running, it prompts to enter a username and password for docker registry. Enter credentials and hit enter.

Then, it starts to install docker and starts the docker daemon.

As soon as the login is successful with the given credentials, it starts pulling nginx docker image from dockerhub.

Once the image is pulled successfully, it starts to spin the container with name nginx-example-docker in port 443

To confirm if nginx image is pulled successfully, run
docker images

To confirm if a container is spinned up to run nginx docker image, run
docker ps -a

Here, you can be able to see docker container with name as nginx-example-docker running in the port 443.

And if you want to confirm, if nginx server is running on port 443, go to the web browser may be chrome or safari (or any other web browser) and enter the public IP address of EC2 instance and append with 443 port For example, https://your-ec2-instance-public-ip:443.

Here, you can see Welcome to Nginx text on the screen.
