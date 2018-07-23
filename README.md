## Tasks
### Part 1: Ansible and basic Linux concepts  - Answers
1. Provisioning of the playbook is broken, you should fix it in order to move forword when everything is working you should get `Ìnstance provisioned successfully` message. Take into account all aspects of the code

Answer: "login_user" and "login_password" had to be added in the file - task/roles/db/tasks/main.yml

2. The system as it is allow all traffic to the server, create a role to limit access to the server via ports 80, 443 & 22 using iptables
Answer: This part is only pending from this tasks. Trying to get this done and push the code, but did not want to waste the time on it.

3. Add http redirection so all traffic will be served via https

Answer: File changed for this tasks is - task/roles/web/templates/nginx/architrave-vhost-ssl.j2 (added the changes on the top of the file)

4. Make sure the client is not receiving the Nginx version as part of the http headers

Answer: "server tokens off" had to be added in the file - task/roles/web/templates/nginx/nginx.conf

5. Create user `testuser` with password `qweRTZ123`

Answer: This file is changed to create an user - task/roles/web/tasks/nginx.yml

6. Change the location of the website files to a more secure folder and grent `testuser` permissions to read the folder content

Answer: This file is changed to create a secure directory, moving the files there and making testuser to view those files - task/roles/web/tasks/nginx.yml
