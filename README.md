Ansible Role: PrestaShop
=========

[![Build Status](https://travis-ci.org/CarlosLongarela/ansible-role-prestashop.svg?branch=master)](https://travis-ci.org/CarlosLongarela/ansible-role-prestashop)

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
    prestashop_db_server: "localhost"
    prestashop_db_name: "prestashop"
    prestashop_db_user: "u_prestashop"
    prestashop_db_password: "p_prestashop"
    prestashop_language: "es"
    prestashop_country: "es"
    prestashop_timezone: "Europe/Madrid"
    prestashop_newsletter: 0

Dependencies
------------

  - CarlosLongarela.mariadb
  - CarlosLongarela.php7
  - CarlosLongarela.nginx

Example Playbook
----------------

    - hosts: servers

      gather_facts: no
      become: true

      vars:
        prestashop_root_path: "/home/webs/prestashop2.test/public"
        prestashop_domain: "prestashop2.test"
        prestashop_timezone: "Europe/Madrid"

      roles:
         - { role: CarlosLongarela.prestashop }

License
-------

GPLv2

Author Information
------------------

This role was created in 2017, May by [Carlos Longarela](mailto:carlos@longarela.eu), from [Taberna WordPress](https://tabernawp.com/).
