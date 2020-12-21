Provisioning a new site
=======================

## Required packages

* nginx
* Python 3
* virtualenv + pip
* Git

eg, on Ubuntu
    sudo-apt-repository ppa:deadsnakes/ppa
    sudo apt update
    sudo apt install nginx git python3.7 python3.7-venv

## Nginx Virtual Host config

* see ngix.template.conf
* replace DOMAIN with, e.g. staging.my-domaincom

## Systemd service

* see gunicorn-systemd.template.service
* replace DOMAIN with, e.g., staging.my-domain.com

## Folder structure

Assume we have a user account at /home/username
/home/username
|__sites
   |--DOMAIN1
   |  |--.env
   |  |--.db.sqlite3
   |  |--.manage.py etc
   |  |--static
   |  |--virtualenv
   |
   |__DOMAIN2
      |--.env
      |--db.sqlite3
      |--etc
