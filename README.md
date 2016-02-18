# LEMP Stack Installation on Ubuntu Server using Ansible
--------
This playbook deploys Nginx, PHP and MySQL(LEMP) on Ubuntu server 14.04 LTS.

## To use this Playbook:

Edit the `/roles/mysql/vars/main` file, in mysql role :

> Change the `mysql_port` & `mysql_bind_address` if you are using non-standard/modified setting. 
>
> Edit the `dbname` for database name.
>
> Edit the `dbuser` for database username.
> 
> Edit the `password` for database user password.

Edit the `/roles/phpmyadmin/vars/main` file, in phpmyadmin role :

> Change the `mysql_root_pass` with your password. 

### Then run this playbook:

```
ansible-playbook site.yml --extra-vars "hosts=192.168.1.78 remote_user=harpreet"
```

**Note:** Don't forget to change `hosts` and `harpreet` with user details. 

To Check apache installation open http://localhost/

To Check PHP installtion open http://localhost/info.php

To Check mysql installtion open http://localhost/phpmyadmin 
