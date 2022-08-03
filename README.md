# Ansible_Kubernetes_on_Azure

Problem Statment:-
* It solves the problem of learning Kubernetes by applying with own hands for novice students to that technology.
* It can be used to deploy in data centers to launch a Kubernetes cluster with just one click of running an Ansible playbook. 
* It automates the process of creating a Kubernetes cluster which will be ready to use in any environment.

Project Description:-

It can solve two use cases:- 
* We all know how big a Kubernetes cluster is and the heavy tasks while setting it up..... And I believe we can learn things as students when we know the internals of any technology and learn it and use them for automating or easing the stuff while we perform real-world operations on that technology. 
* For that, I have created this setup which will be useful to students to understand the cluster from within where they can open every file and operate every pod in the master different from the third party provider who only gives access to use it but not changing the internals. 
* And for the companies it is not simple to implement new technology without the person who can execute it...So I have automated the whole setup which can be done with a single click

Deployment Steps:-
1. For automating the configuration of the Kubernetes Cluster we are using Ansible as a configuration and management tool so we have to install the Ansible package in an instance with the required python environment already set up in the same instance.
2. For launching the Kubernetes cluster...we have to create virtual machines in the azure with any distribution of Linux because Ansible is independent of OS while configuring the server.
3. And we have to update the ansible inventory with the IPs of our Kubernetes master and slaves nodes then have to check the connectivity.
4. And based on the requirement of the type of Kubernetes cluster we have to use...we have to write our script accordingly in the YAML file separately for master and slave nodes of Kubernetes.
5. And writing the script for exchanging the authentication token between the master and slaves is critical...so we can have to use the preferred way to exchange them and execute.
6. For setting up the environment the files that I have kept in the repository and enough with your key to the instance should be updated in the ansible inventory.
7. Important thing is...while setting up the cluster the environment might be different in several instances and versions...so have to check and resolve them and my project is mainly focused on setting up the whole cluster environment on the azure virtual_machine_instances.


DEMO_URL = https://drive.google.com/file/d/1qPjziXezktq2VgMCz4JOqlFEbvchqpSv/view?usp=sharing

Files Description:-

1. ansible.cfg :- ansible.cfg :- This file is useful to set up the required things for the ansible in the configuration file like setting up the python environment
2. master.yml :- This yml file is useful to configure the whole Kubernetes master node including the flannel overlay network
3. slave.yml :- This file is useful to configure the slaves and to join the cluster initiated by the master with the help of a token provided by the master
4. ip.txt :- this is the inventory file for the ansible from where it gets the IP address of the nodes where it should operate with the help of python 
5. kub.sh :- Useful to create a repo file for the Kubernetes and to install the required packages
6. docker.repo:- file which should be kept in /etc/yum.repos.d for configuring yum to install the docker-ce package


