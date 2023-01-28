# Makefile

.PHONY: dumvars ping ev site halt ac uk pioff

dumpvars:
	ansible -m debug -a 'var=hostvars[inventory_hostname]' all

ping:
	ansible all -m ping

ev:
	ansible-vault edit group_vars/all/vault

site:
	ansible-playbook site.yml

halt:
	ansible all -u root -a "/sbin/shutdown -h now"

ac:
	ansible-playbook ansible-control.yml

uk:
	ansible-playbook all.yml --tag uk

pioff:
	ansible espdev -u root -a "/usr/bin/sudo /sbin/shutdown -h now"
