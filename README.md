# RIDING BYTES Ansible - Odoo

A set of [Ansible][4] roles to deploy a [RIDING BYTES][1] approved server
environment for [Odoo][2].

A [RIDING BYTES][1] approved server environment includes the following
components:

- Initial server setup
- PostgreSQL
- Odoo 9
- NGINX
- Firewall

Custom [Ansible Roles][6] are located in the `roles` directory. Each `role`
contains a `README.md` with further documentation.


## Getting Started

Install dependencies from [Ansible Galaxy][2]:

    ansible-galaxy install -r requirements.yml

Create an [Ansible Playbook][5] and name it `custom.yml` (excluded in `.gitignore`):

    ---
    - hosts: all
      become: yes
      gather_facts: yes
      roles:
        - role: ridingbytes_odoo

Create an [Ansible Inventory][8] file, e.g. name it `custom_hosts.cfg` (excluded
in `.gitignore`):

    [local]
    127.0.0.1

Run your custom [Ansible Playbook][5]:

    ansible-playbook -i custom_hosts.cfg custom.yml

Please refer to the `vagrant.yml` [Ansible Playbook][5] for a working example.


## Vagrant

This repository contains a running [Vagrant][3] setup, which creates a full
[Odoo][2] installation on an Ubuntu Trusty 64-bit server.


### Vagrant Setup

Install dependencies from [Ansible Galaxy][2]

    ansible-galaxy install -r requirements.yml

Start the [Vagrant][3] machine:

    vagrant up

This will download a Linux machine according to the `Vagrantfile` within this
repository.

Note: The server will listen on `192.168.22.10`.

As soon as the machine is running, you can start the provisioning process:

    ansible-playbook -i vagrant_hosts.cfg vagrant.yml

> Depending on your configuration, you may need to edit the vagrant_hosts.cfg
> and change the location of the private_key file that is used.

As soon as the [Ansible Playbook][5] is done, you can open a browser and
navigate to: http://192.168.22.10



[1]: http://ridingbytes.com "RIDING BYTES"
[2]: https://odoo.com "Odoo ERP"
[3]: https://www.vagrantup.com/docs/getting-started/ "Vagrant"
[4]: https://www.ansible.com "Ansible"
[5]: https://docs.ansible.com/ansible/playbooks.html "Ansible Playbook"
[6]: https://docs.ansible.com/ansible/playbooks_roles.html "Ansible Roles"
[7]: https://galaxy.ansible.com "Ansible Galaxy"
[8]: https://docs.ansible.com/ansible/intro_inventory.html "Ansible Inventory"
