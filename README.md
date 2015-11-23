To use


Install using vagrant
----------------------

Edit the Vagrantfile so the base box points to something you have

Do vagrant up and ansible will run automaticly


Install using Ansible:
----------------------

create an inventory file with the name of the machine to use

Run
ansible-playbook -i inventory test.yml


