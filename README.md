# ansible ubuntu
## Overview
Following a new Ubuntu build, install favourite apps. 

##Pre-reqs
Install ansible, git & clone this code:

    sudo apt-get install ansible
    sudo apt-get install git
    $ mkdir ansible
    $ cd ansible/
    $ git clone https://github.com/jonomcclelland/ansible_ubuntu
    $ cd ansible_ubuntu

## Prepare inventory
Modify the inventory file if you need to add remote hosts. Just add the dns or IP addresses of targets. Otherwise, it defaulst to the localhost over direct (not ssh) connection.

## Install all apps
    ansible-playbook -vvvv -i inventory -s site.yml -kK


## Install all virtual machine apps
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=virtual


## Install all desktop apps
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=desktop


## Install a specific app
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=chrome
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=sublimetext
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=virtual
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=vagrant
    ansible-playbook -vvvv -i inventory -s site.yml -kK --tags=terraform


