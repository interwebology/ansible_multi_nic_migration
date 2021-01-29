# Centos 6 to 7 Transcoder Backup and Install Ansible Playbook

A simple Ansible configuration to pull the networking configurations and repos from CentOS boxes hosting transcoder software (multiple NICs). 

For transcoder upgrades from Centos 6 to Centos 7 because it will pull down configs for NIC names like 'eth0' and rewrite to the CentOS7 NIC with the 'enp6s0' type names

The install script will install the NIC configs and put transcoder user into sudoers file per user request. 
