## Ping module
```bash
# add controller as the host machine
sudo vi /etc/ansible/hosts
localhost
ansible all -m ping -o # if we want to print output in a single line
```
## Shell module
* https://docs.ansible.com/ansible/2.8/modules/shell_module.html#shell-module
  ```bash
  ansible all -m shell -a "date"
  ansible all -m shell -a "uptime"
  ansible all -m shell -a "df -h"
  ```

## yum module
* if you want to excute/install on a single node, availiable in the host file ,we can use the below syntax.
```bash
ansible <ip-address> -b -m yum -a "name=tree"
anible 172.29.124.267 -b  -m yum -a "name=tree"

ansible -i inv 10.XX.XX.XX -b -m yum -a "name=httpd"
```
## service module
* https://docs.ansible.com/ansible/latest/collections/ansible/builtin/service_module.html
```bash
ansible -i inv 10.XX.XX.XX -b -m service -a "name=httpd state=started"
```
## Copy modue
vi log.txt
there is a log file created by splunk
* https://docs.ansible.com/ansible/latest/collections/ansible/builtin/copy_module.html
 ```bash 
ansible -i inv -b -m copy -a "src=log.txt dest=/tmp/log.txt"
```
