To use


Using testing environment
----------------------

In `tests/` is a working vagrant setup.

Edit the Vagrantfile so the base box points to something you have

Do `vagrant up` and ansible will run automaticly


For real: install using Ansible
----------------------

I suggest using `test.yml`from the tests directory a base, and overload the values in `defaults/main.yml`.

Currently:

* To enable services, they must be "true" in defaults/service and in the services list.

* Currently: RabbitShare, PythonOnPills and Bashtard may be installed using this role


When it is installed

Start the system by running

    cd ~/CTFd_local
    nodejs /opt/CTFd/bin/ctfd.js config.js
    
to start the game

    daemon.start()
