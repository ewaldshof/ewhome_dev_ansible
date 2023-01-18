# Makefile

.PHONY: dumvars ping ev site halt

dumpvars:
	ansible -m debug -a 'var=hostvars[inventory_hostname]' all

ping:
	ansible all -m ping -u service

ev:
	ansible-vault edit group_vars/all/vault

site:
	ansible-playbook site.yml

halt:
	ansible all -u root -a "/sbin/shutdown -h now"
