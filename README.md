
## pre

```
vagrant box add centos6.7 https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box
```

## setup(ssh key)

### client

```
sudo yum install ansible vim -y

cd ~/.ssh
ssh-keygen -t rsa

# set target hosts
vim /etc/ansible/hosts

# XXX.XXX.XXX.XXX ansible_ssh_user=vagrant ansible_ssh_private_key_file=/home/vagrant/.ssh/id_rsa
```


### server1,2

```
sudo yum install vim -y

# copy id_rsa.pub from client

# add pub_key of client(user vagrant)
vim ~/.ssh/authorized_keys

# rsa-XXXX vagrant
```

### setup check

ansible-playbook /vagrant/playbooks/ping.yml


