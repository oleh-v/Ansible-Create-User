# [Ansible](https://www.ansible.com). Create User (interactive)

![Ansible](https://cdn.slidesharecdn.com/profile-photo-ansible_it-96x96.jpg)

This playbook create User and copy public key (if exist) or Generate keys pair on target machine
* Adding a New User
* Grant "Sudo" privileges
* Change primary group
* Add to additional groups
* Generate keys pair or copy existing key

## Compatibility
* CentOS
* Ubuntu

## Requirements
* SSH root access to the target servers. 

How to do that: Copy your public key to the target server with command below:
```
ssh-copy-id root_user@target.server.com
```

## Usage
* In `./ansible.cfg` - check path to your private key and username 
* (optional) Copy existing public_key of new User if you have to `./keys/` directory with name format `username.pub`
* Run Playbook:
```
ansible-playbook adduser.yml
```
* Answer to the questions while playbook is running.
* (Generated key pairs will be also copied locally `./keys/` ) 
