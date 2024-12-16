## Create the web server in ubuntu
```bash

# update the repo
sudo apt update

# install apache2
sudo apt install apache2 -y

# default html file

echo "Ansible Learning" > /var/www/html/index.html
```

* Here are the list of modules [availiable](https://docs.ansible.com/ansible/2.8/modules/list_of_all_modules.html)
* For apt modules [click here] (https://docs.ansible.com/ansible/2.8/modules/apt_module.html#apt-module)
* we need to pass the parameters based on the module
* Let try to create the relevant ansible format for the above manual steps.
     * We have choose the apt module, and we need to pass the below parameters:
           * name: apache2
           * state: present
           * update_cache: yes
* Using the above arrguments, now we need to infrom ansible to excute,
  * we can do this activity by 2 ways
     * adhoc
     * playbooks
## adhoc commands
ansible -b -i inv -m apt -a "name=apache2 state=present update_cache=yes"

       
       
