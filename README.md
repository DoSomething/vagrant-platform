DoSomething.org website platform
================

Ansible provisioning for the Drupal 7 platform Vagrant

Usage
================

- Clone the repository
- Create `.vault.txt` with shared password to decrypt Ansible Vaults
- Download playbooks:  
  `ansible-galaxy install -r requirements.yml -p ansible/roles --force`
- Run `vagrant up`

Contribution
================

Changes must be made in according role repositores.  
You can make test changes directly in `ansible/roles`, but don't forget
to move them into accoring repos.

To test your changes, run `vagrant provision`.
