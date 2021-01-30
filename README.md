# Centos 6 to 7 Transcoder Backup and Install Ansible Playbook

A simple Ansible configuration to pull the networking configurations and repos from CentOS 6 boxes with multiple NICs like you would see with transcoders 

For transcoder upgrades from Centos 6 to Centos 7 it will pull down configs for NIC names like 'eth0' and rewrite to the CentOS 7 NIC configuration with the 'enp6s0' nameing conventions.

The install script will install the NIC configs and the grab script with pull down the configs you are looking to backup.

## Grabbing the NIC configurations and repos from CentOS 6

Simply run **ansible-playbook grab_configs.yml -i host.txt -u root --ask-pass**

## Installing the NIC configurations to CentOS 7

Run ***ansible-playbook install_config.yml -i host.txt -u root --ask-pass**

if you get the common error where Ansible has trouble interacting with libselinux then you will need you install it.

**sudo yum install -y libselinux-python**
