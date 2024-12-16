## Install Ansible
```bash
# Login with root user and create a user called ansible (any user it's your wish) and this user should be having sudo permissions on all the server.
# Creting a user called asnible on the hosts (both controller and nodes)
useradd ansible
passwd ansible

# We need the nessary changes in sudo file, so ansible use can go with sudo and also with password lesss access.
visudo
## Same thing without a password
# %wheel ALL=(ALL)    NOPASSWD: ALL
ansible  ALL=(ALL)    NOPASSWD: ALL

# Next, by deafult these machines can't be logged in from outside, so make sure the password based authonetication is enabled
vi /etc/ssh/sshd_config
# To disabled tunneled clear text passwords, change to no here !
PasswordAuthentication yes

# Restart the sshd service
service sshd restart

# Install the  Ansible on the Controller only.
yum install ansible -y
```
## Configure ansible

```bash
```

## Generate ssh key
```bash
# Generate the ssh key in the ansible server
ssh-keygen
yes
yes

# Even though we have the key generated, still connecting to the host machine it's asking for the password
# Now, copy the key generated to the host machine as the ansible user.

ssh-copy-id username@privateip
```

## Test the ansible Installation
```bash
# ansible need to the host machine details to communicate and perform certain tasks
# The default host/inventory file is availiable at this location

vi /etc/ansible/hosts
 ansible -m ping all
```
