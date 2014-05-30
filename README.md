marklee77.mariadb
=================

[![Build Status](https://travis-ci.org/marklee77/ansible-role-mariadb.svg?branch=master)](https://travis-ci.org/marklee77/ansible-role-mariadb)

MariaDB role for Ubuntu.

Role Variables
--------------

- mariadb_repository_mirror: mariadb repository mirror, set to 
                             http://mirrors.coreix.net/mariadb by default.
- mariadb_version: mariadb version, set to 10.0 by default.
- mariadb_root_mysql_password: root mysql password; set to a random value by 
                               default.

Example Playbook
-------------------------

    - hosts: default
      roles:
        - marklee77.mariadb

License
-------

GPLv2

Author Information
------------------

http://marklee77.github.io/
