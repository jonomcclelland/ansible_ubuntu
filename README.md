Overview
========

Following a new Ubuntu build, install favourite apps. 

Install all apps
----------------
ansible-playbook -vvvv -i inventory -s site.yml

Install all desktop apps
------------------------
ansible-playbook -vvvv -i inventory -s site.yml --tags=desktop

Install all virtual machine apps
--------------------------------
ansible-playbook -vvvv -i inventory -s site.yml --tags=virtual
