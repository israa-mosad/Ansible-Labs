## Summary:

Explore ansible installation and Inventory file.

## Steps:

•	Check Ansible installation.
-     ansible --version

•	Check Inventory path

-     vi /etc/ansible/hosts

•	Add new managed host to the Inventory then save and exit

-      [webservers]
-      Webserver1 <client hostname>=<client IP> ansible_user=cloud

 ### Eg:

-      [webservers]
-      Webserver1 ansible_host=192.168.66.189 ansible_user=cloud
