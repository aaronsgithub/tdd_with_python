Provisioning a new site
=======================

Assuming OS is Ubuntu 14.04

## Required packages:

* nginx
* Git


eg, on Ubuntu 14.04:

    sudo apt-get install nginx git

Other third party software to be installed via git:

* pyenv
* pyenv-virtualenv

Then create a virtualenv and install any required python modules using pip.

## Nginx Virtual Host config

* see nginx.template.conf
* replace SITENAME with, eg, staging.my-domain.com

## Upstart Job

* see gunicorn-upstart.template.conf
* replace SITENAME with, eg, staging.my-domain.com

## Folder structure:
Assume we have a user account at /home/username

/home/username
└── sites
    └── SITENAME
         ├── database
         ├── source
         ├── static
         └── virtualenv
