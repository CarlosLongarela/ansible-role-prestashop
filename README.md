Ansible Role: PrestaShop
=========

[![Build Status](https://travis-ci.org/CarlosLongarela/ansible-role-prestashop.svg?branch=master)](https://travis-ci.org/CarlosLongarela/ansible-role-prestashop)
[![Percentage of issues still open](http://isitmaintained.com/badge/open/CarlosLongarela/ansible-role-prestashop.svg)](http://isitmaintained.com/project/CarlosLongarela/ansible-role-prestashop "Percentage of issues still open")
[![Average time to resolve an issue](http://isitmaintained.com/badge/resolution/CarlosLongarela/ansible-role-prestashop.svg)](http://isitmaintained.com/project/CarlosLongarela/ansible-role-prestashop "Average time to resolve an issue")

Prestashop 1.7.1 install and configuration.

Requirements
------------

None.

Role Variables
--------------

    prestashop_version: 1.7.1.1
    prestashop_url_download: "https://download.prestashop.com/download/releases/prestashop_{{ prestashop_version }}.zip"

    prestashop_root_path: "/home/webs/prestashop.test/public"

    prestashop_domain: "prestashop.test"
    prestashop_db_create: 1
    prestashop_db_clear: 1
    prestashop_db_server: "localhost"
    prestashop_db_name: "prestashop"
    prestashop_db_user: "u_prestashop"
    prestashop_db_password: "p_prestashop"
    prestashop_db_engine: "InnoDB"
    prestashop_db_prefix: "ps_"
    prestashop_language: "es"
    prestashop_country: "es"
    prestashop_timezone: "Europe/Madrid"
    prestashop_newsletter: 0

    prestashop_firstname: "PrestaShop"
    prestashop_lastname: "Developer"
    prestashop_password: "p_prestashop"
    prestashop_email: "dev@prestashop.com"

    prestashop_admin_folder_name: "adminpr2791"
    prestashop_check_file_name: "prestashop-installed.txt"

Dependencies
------------

  - [CarlosLongarela.percona](https://galaxy.ansible.com/CarlosLongarela/percona/)
  - [CarlosLongarela.mariadb](https://galaxy.ansible.com/CarlosLongarela/mariadb/)
  - [CarlosLongarela.php7](https://galaxy.ansible.com/CarlosLongarela/php7/)
  - [CarlosLongarela.nginx](https://galaxy.ansible.com/CarlosLongarela/nginx/)

Example Playbook
----------------

    - hosts: servers

      gather_facts: no
      become: true

      vars:
        prestashop_root_path: "/home/webs/prestashop2.test/public"
        prestashop_domain: "prestashop2.test"
        prestashop_timezone: "Europe/Madrid"
        prestashop_admin_folder_name: "pradmin2791"

      roles:
         - { role: CarlosLongarela.prestashop }

License
-------

GPLv3

Author Information
------------------

This role was created in 2017, May by [Carlos Longarela](mailto:carlos@longarela.eu), from [Taberna WordPress](https://tabernawp.com/).
