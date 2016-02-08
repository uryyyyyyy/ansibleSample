
## setup(ssh key)

### client

```
cd ~/.ssh
ssh-keygen -t rsa

# set target hosts
vim /etc/ansible/hosts

# XXX.XXX.XXX.XXX ansible_ssh_user=vagrant ansible_ssh_private_key_file=/home/vagrant/.ssh/id_rsa
```


### server1,2

```
# add pub_key of client(user vagrant)
vim ~/.ssh/authorized_keys

# rsa-XXXX vagrant

```

