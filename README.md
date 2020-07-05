![image](https://user-images.githubusercontent.com/38517925/86527948-5f983e80-bec1-11ea-9be7-03a6cc7792c8.png)

# INTRODUCTION
---------------

This playbook is intended to install and configure *Puppet 6* on RHEL/CentOS 7 only currently.

Read this document carefully to have more understanding about this ansible playbook.

![image](https://user-images.githubusercontent.com/38517925/86531925-2b357a00-bee3-11ea-8c93-57e9248812ac.png)

## VARIABLES DECLARATION
-----------------------

Variables need to declared inside playbooks/vars/main.yml

1. **puppetRepo** => Repository path to download packages, either you can leave it as default or set your custom path.

2. **master** => Node name or FQDN which you want to set as your puppet master.

###### INVENTORY SETUP

One can use it's own inventory or create it's own inventory. Replace the hostnames in "inventory" file present here with hostnames of your environment. 

# USAGE
------------------------

Step | Description | Commands
------ | ----------- | --------
1 | Download this playbook in your ansible server | # git clone https://github.com/HemantGangwar/puppetSetup.git
2 | Enter into the directory created | # cd puppetSetup
3 | Update inventory file provided here with your node names. | # vi inventory
4 | Update playbooks/vars/main.yml with required parameter | (example) puppetRepo: https://yum.puppet.com/puppet6-release-el-7.noarch.rpm 
->  |  | master: master.lab.example.com
5 | Now execute the playbook | # ansible-playbook playbooks/puppet.yml


Note:  *The playbook is fully idempotent and can be safely used multiple times.*

AUTHOR
--------
This playbook is written by Hemant Gangwar, you can read more about author at https://learningtechnix.wordpress.com or follow on LinkedIN https://www.linkedin.com/in/hemant-gangwar-6a677b19/
