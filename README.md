Ansible Role: Prestashop
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

      roles:
         - { role: CarlosLongarela.prestashop }

License
-------

GPLv2

Author Information
------------------

This role was created in 2017, May by [Carlos Longarela](mailto:carlos@longarela.eu), from [Taberna WordPress](https://tabernawp.com/).
