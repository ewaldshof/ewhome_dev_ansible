# ewhome_dev_ansible
Development environment with rasbian for ewhome

# Ansible
Change to ansible directory

## Adding a new host to inventory for staging

1. Certificate must be installed on remote and local
2. $ ssh root@<host_ip> # succeeds without asking for password
3. $ ssh-keyscan <host_ip> >> ~/.ssh/known_hosts # Server must be up and sshd running
4. Add to inventory.ini
5. $ make ping
6. $ make site

