# Ansible e-commerce application playbook

This is an ansible playbook to complete the project proposed in the course [Ansible for the Absolute Beginner - Hands-On - DevOps](https://www.udemy.com/course/learn-ansible/).

The project consists on the deployment an small web application using the LAMP stack. First we have to configure the environment and deploy the application manually and then we have to automate that process using Ansible.

The application that is deployed can be found here: https://github.com/kodekloudhub/learning-app-ecommerce

You can find a fork of the application repository here: https://github.com/JRuedas/learning-app-ecommerce

I have set up 2 CentOS Virtual Machines (VBox) in order to have multiple workers. My own PC takes the role of the Ansible controller.

## Prerequisites
The following Ansible modules must be installed:
- community.mysql
- ansible.posix

The `inventory.txt` file must contains a `webserver` and a `dbserver` host. Both hosts can be the same.

To run the playbook execute: 
>    ansible-playbook playbook-learning-app-ecomerce.yaml -i inventory.txt --ask-become-pass
