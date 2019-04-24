# password-less-ssh
# Ansible Playbook to enable passwordless ssh login between Ansible control machine and nodes

Using this playbook we can enable passwordless ssh login between ansible control machine and nodes. Using this single playbook we can enable this password login to N number of nodes simultaneously.

Instruction:
------------

Below variables need to be changed/added based on the environment in config.yml file

1. id_rsa_file - This is the RSA private key which will be generated or used if already existing. You can change this if using some other rsa key
2. passphrase - This is the passphrase of generating rsa key
3. root_password - RSA key is generated for root user in control machine. This will be the root password for the nodes if they are using common root password
4. nodes - This will be the list of nodes for which passwordless authentication will be enabled. You can add any number of nodes under this section

Above 4 variables can be modified according to user's needs

Executing playbook:
-------------------

# ansible-playbook password-less-ssh.yml
