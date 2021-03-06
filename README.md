Linux Server Configuration
======================================

Project 5 for Udacity Full Stack Nano Degree.

A linux server is cofigured to run Apache HTTP server and host a Python application made with Flask.


Log In
--------------------------------------
- **IP Address:** 52.27.217.246
- **SSH Port:** 2200


URL to the Hosted Web Application
---------------------------------------
[http://ec2-52-27-217-246.us-west-2.compute.amazonaws.com](http://ec2-52-27-217-246.us-west-2.compute.amazonaws.com)


Installed Software
---------------------------------------
- apache2
- libapache2-mod-wsgi
- python-setuptools
- postgresql
- postgresql-contrib
- fail2ban
- apticron
- glances
- git


Configuration Changes
---------------------------------------
- Created user "grader" with sudo permissions.
- Disabled root user remote log in.
- Key-based SSH authentication is enforced.
- All installed packages were updated.
- Timezone set to UTC.
- Changed SSH port to 2200.
- Configured firewall to only allow incoming connections through ports 2200, 80, and 123. All outgoing connections are allowed.
- Unsuccessful log in attempts are monitored. Consective 3 unsuccessful login attempts within 10 minutes will be banned for 1 hour. An email notification will be sent to the administrator.
- Configured to check package updates daily. Downloads but will not install. An email notification will be sent to the administrator if there are new updates available. The local download archive is cleaned every week.
- Installed Glances for system monitoring.
- Configured Apache to serve a Python mod_wsgi application.
- Remote connections to PostgreSQL are not allowed.
- A PostgreSQL user named "catalog" was created with limited permisions.


Resources
---------------------------------------
- [SSH Keys](https://wiki.archlinux.org/index.php/SSH_keys)
- [SSH/OpenSSH/Configuring](https://help.ubuntu.com/community/SSH/OpenSSH/Configuring)
- [How To Install and Use PostgreSQL on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04)
- [mod_wsgi (Apache)](http://flask.pocoo.org/docs/0.10/deploying/mod_wsgi/)
- [How To Protect SSH with Fail2Ban on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-protect-ssh-with-fail2ban-on-ubuntu-14-04)
- [Automatic Updates](https://help.ubuntu.com/lts/serverguide/automatic-updates.html)
- [Glances](https://github.com/nicolargo/glances/blob/master/docs/glances-doc.rst)

