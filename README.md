# SSH-Access
Grant/Revoke SSH access to new developer

# Execute below command to add new user and grant SSH access

ansible-playbook -i servers/ -e "action=grant" playbook/ssh.yml

# Execute below command to remove user and revoke SSH access

ansible-playbook -i servers/ -e "action=revoke" playbook/ssh.yml

# Execute below command to grant SSH access only if user created separtely

ansible-playbook -i servers/ -e "action=grant" playbook/ssh.yml --skip-- tags=add

# Execute below command to revoke SSH access only and don't need to remove user

ansible-playbook -i servers/ -e "action=revoke" playbook/ssh.yml --skip-- tags=remove
