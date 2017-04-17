##http://cloudacademy.com/blog/building-ansible-playbooks-step-by-step/##
Deploying Simple HTML Page
*************************************
To deploy a simple HTML page, we need to ensure that apache is installed and configured on our host machine. So therefore, in this section we will:
*************************************
--->install Apache
--->start the Apache service
--->deploy a static webpage with images – This static webpage will leverage Ansible templates where it will display the text “Thank you for reading this post. My IP Address is <ip-address-of-instance>” and Ansible logo. To fetch the IP address of host, it will rely on Ansible Fact
--->restart Apache once the deployment is over
*************************************
let’s have a look at the high-level structure of this simple Ansible 
site.yml – starting point of our ansible playbook
hosts – carrying hosts information
roles/ - defining what each type of server has to perform
       webservers/
              tasks/ - tasks performed on webservers
                     main.yml
              handlers/ - running tasks under particular events
                     main.yml
              templates/ - configuration files which can reference variables
                     index.html.j2
              files/ - files to be copied to webservers
                     ansible.png
