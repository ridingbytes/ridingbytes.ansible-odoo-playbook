# RIDING BYTES Base Role

This role provisions all requirements for a system to run [Odoo][1].

This role takes care of:

- Updating the Distribution
- Upgrading the Distribution
- Installing the required OS packages for [Odoo][1]

## Dependencies

None

## Role Variables

Available variables are listed below, along with default values (see
`defaults/main.yml` and `vars/{{ ansible_distribution }}.yml`):

    apt_update_package_lists: 1
    apt_download_upgradable_packages: 1
    apt_autocleaninterval: 7
    apt_unattended_upgrade: 1

Variables consumed by the template `10periodic.j2`, which gets copied to the `{{ apt_conf_dir }}`.
> Note: Set `apt_periodic: no` to disable.


[1]: https://odoo.com "Odoo"
