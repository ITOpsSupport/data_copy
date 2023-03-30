created by: Ayush Raj
Date: Mar 30 2023
Requirement:
Download datafrom remmote source and copy it locally 
    a. The file name should be taken from /etc/ansible/hosts
    b. copy path /etc/systemd/system/*
    c. desination location /tmp/downloads of locale machine 

Note : I have used time module to fix the duplicate issue even if the playbook is getting run multiple times.

################ 

How to execute this playbook 

1. make a group [bifix] in /etc/ansible/hosts # I have assumed the greou name as bigfix
2. write hosts in below mentioned pattern
[bigfix]
192.168.1.14  # add your target host 
192.168.1.15

3. to run 
# python3 /usr/bin/ansible-playbook fetch_data_remote_local.yaml -u root -k

4. when prompt for password , enter your root password 

5. Once playbook run successfully , you can check your /tmp/downloads/ of your local machine from which playbook is being executed.

