# homelab_new_DC
Configures a stock Windows server into a domain controller.
The goal of this project is to set up a new domain controller with users and groups for use in a homelab. 
This has been tested against Windows Server Core 2022 and ran from a Debian server. Should be compatible with Windows Server 2016+ and any Linux server with Ansible installed.

Steps to creating the domain controller:
- Create passwords.yml file with the variables commented out in the variables section of the NEW_DC_PLAYBOOK.yml
- Encrypt the passwords.yml file with Ansible-Vault
- Copy the passwords.yml and NEW_DC_PLAYBOOK.yml to the Ansible server
- Set up the hosts file as per the example hosts file in this repo
- Customize your variables at the top of the NEW_DC_PLAYBOOK.yml file
- Run ansible-playbook NEW_DC_PLAYBOOK.yml --ask-vault-pass

Enjoy your new domain controller, groups, and users!
