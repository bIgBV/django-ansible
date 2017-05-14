## Django-ansible
This is a simple setup for deploying django apps running postgres using uwsgi and nginx.

To run this file you need to:

* Fill in the various variables according to your specific project in the file `env_vars/base.yml`. 
* Following that you need to add the public/private ssh keys used to access the git repository in the root directory and name them `deploy_key`, `deploy_key.pub`. 
* Modify the contents of  `ansible-cfg/hosts` to the ip's  of your server and copy the contents of the file over to `/etc/ansible/`

Then all you have to do is run

    ansible-playbook -s vagrant.yml -u vagrant -vv

To test the setup out in a ubuntu 14.04 vagrant box, or

    ansible-playbook -s web.yml -u ubuntu -vv

To provision a server and deoploy your app on it.
