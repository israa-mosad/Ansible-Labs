## Summary: 

•	Create a playbook to install and enable HTTPd service.

## Steps: 
1- 	Check the managed host and make sure that no httpd is installed
-       rpm -qa httpd

2-Create a new directory to hold the playbook and inventory files.
-     mkdir apache-project
-     cd apache-project
-     mkdir inventories
-     cd inventories
3-	Create a playbook file then save and exit

4- $ vi hosts
-     [webservers]
-     Webserver1 ansible_host=192.168.98.195 ansible_user=cloud ansible_ssh_private_key_file=/etc/ansible/client.pem 

5- Create a playbook file then save and exit
-     vi apache-playbook.yml
-     content in link below
     https://github.com/israa-mosad/Ansible-Labs/blob/main/lab-2/apache-playbook.yml
     
 6- Run the playbook
-     $ ansible-playbook apache-playbook.yml -i inventories/hosts

7- Check the managed host and make sure that httpd is installed
-     $ rpm -qa httpd
8- Check the httpd service status
-     $ systemctl status httpd
-     $ curl http://192.168.98.195 > client 
9-Check the httpd service via curl by the managed host IP address.

10-Create index.html file in the same directory of the playbook.
-    content in link below : https://github.com/israa-mosad/Ansible-Labs/blob/main/lab-2/index.html

11- Rerun the playbook
-     $ ansible-playbook apache-playbook.yml -i inventories/hosts
12-	Check the httpd service via curl by the managed host IP address.
-     	curl http://192.168.98.195


    
