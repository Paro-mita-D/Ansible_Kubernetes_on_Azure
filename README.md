# Ansible_Kubernetes_on_Azure
1. ansible.cfg :- ansible.cfg :- This file is useful to setup the required things for the ansible in the configuration file like setting up the python environment
2. master.yml :- This yml file is useful to configure the whole Kubernetes master node including the flannel overlay network
3. slave.yml :- This file is useful to configure the slaves and to join the cluster intiated by the master with the help of token provided by the master
4. ip.txt :- this is the inventory file for the ansible from where it gets the IP address of the nodes where it should perform operation with the help of python 
5. kub.sh :- Useful to create a repo file for the Kubernetes and to install the required packages
6. docker.repo :- file which should be kept in /etc/yum.repos.d for configuring yum to install docker-ce package
