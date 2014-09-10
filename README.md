marklee77.development
=====================

FIXME!

[![Build Status](https://travis-ci.org/marklee77/ansible-role-chrony.svg?branch=master)](https://travis-ci.org/marklee77/ansible-role-chrony)

Chrony role for Ubuntu.

Role Variables
--------------

- chrony_ntp_servers: list of ntp servers, set to a selection from pool.ntp.org 
    by default.

Example Playbook
-------------------------

    - hosts: all
      roles:
        - marklee77.chrony

License
-------

GPLv2

Author Information
------------------

http://marklee77.github.io/
