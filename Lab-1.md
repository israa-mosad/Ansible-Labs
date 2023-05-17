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
 
 ## Note:-
 The " hosts file " is an inventory file that Ansible uses to determine which hosts to connect to. 
 
 The file is divided into groups, and each group contains a list of hosts. 
 
 In the example you provided, there is a single group called webservers that contains a single host called Webserver1.
