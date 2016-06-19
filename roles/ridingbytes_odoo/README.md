# RIDING BYTES: Odoo Role

This role provisions [Odoo][2].

This role istalls [Odoo][2] using the [Odoo Ansible Role][9] and
configure it on the remote machine.

## Dependencies

This role depends on the follwoing Ansible Roles:

- RIDING BYTES: PostgreSQL Role
- [PostgreSQL Ansible Role][10]
- [Odoo Ansible Role][9]

## Role Variables ##

Please refer to the [Odoo Ansible Role][9] for available variables.
This role customizes the following variables in `vars/main.yml`:

    odoo_service: odoo
    odoo_version: 9.0
    odoo_repo_rev: "saas-9"


[1]:  http://ridingbytes.com "RIDING BYTES"
[2]:  https://odoo.com "Odoo ERP"
[3]:  https://www.vagrantup.com/docs/getting-started/ "Vagrant"
[4]:  https://www.ansible.com "Ansible"
[5]:  https://docs.ansible.com/ansible/playbooks.html "Ansible Playbook"
[6]:  https://docs.ansible.com/ansible/playbooks_roles.html "Ansible Roles"
[7]:  https://galaxy.ansible.com "Ansible Galaxy"
[8]:  https://docs.ansible.com/ansible/intro_inventory.html "Ansible Inventory"
[9]:  https://galaxy.ansible.com/sebalix/odoo "Odoo Ansible Role"
[10]: https://galaxy.ansible.com/ANXS/postgresql "PostgreSQL Ansible Role"
