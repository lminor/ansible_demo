# Ansible Demo
A quick spinup dev environment to deploy the latest release version of Laravel to a Vagrant server.

## Vagrant Installation Instructions

1. Make sure virtualbox is installed [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
2. Make sure vagrant is installed [Vagrant](https://www.vagrantup.com/downloads.html)
    * Basic Vagrant instructions can be read here for further information (https://www.vagrantup.com/docs/getting-started/)
3. Make sure Ansible is installed [Ansible](http://docs.ansible.com/ansible/intro_installation.html)
    * For use on Mac I use [Homebrew](https://brew.sh/) *brew install ansible*
3. Download this repository to your ~/VM folder or other preferred Vagrant folder.
4. Using Terminal navigate to the root of this folder and run "vagrant up".

## Encrypted variables
- We use Ansible Vault to encrypt passwords/keys in the repository. More info can be found here [Ansible Vault](http://docs.ansible.com/ansible/playbooks_vault.html)
- If the host_vars/ansible-demo.dev/secret.yml file is encrypted then request to be shared on the encryption file which further instructions will be given at that time for setup.
- If the host_vars/ansible-demo.dev/secret.yml file is not encrypted you should make sure that you encrypt it before committing the file to your own repository.

## Install Ansible Galaxy dependencies
Run the following command to install dependencies
* *ansible-galaxy install -r requirements.yml*

## Run Ansible Install
This will build all server dependencies and install the code base along with database on your vagrant machine.
- Using Terminal navigate to the root of this folder and run *ansible-playbook server_setup.yml --extra-vars "host=ansible-demo.dev"*
- Navigate to [ansible-demo.dev](http://ansible-demo.dev) to see your local ansible install

## TLDR
1. ```ansible-galaxy install -r requirements.yml```
2. ```vagrant up```
3. ```Set variables in host_vars/ansible-demo.dev/secret.yml```
4. ```ansible-playbook server_setup.yml --extra-vars "host=ansible-demo.dev```
5. Navigate to [ansible-demo.dev](http://ansible-demo.dev) to see your local ansible install
