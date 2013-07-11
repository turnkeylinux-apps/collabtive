Collabtive - GroupWare
======================

`Collabtive`_ is web-based project management software intended for
small to medium-sizes businesses and freelancers. It is an open Source
alternative to proprietary tools like Basecamp. Key features include
tracking of projects, milestones, and tasks, importing from Basecamp,
timetracking and reporting.

This appliance includes all the standard features in `TurnKey Core`_,
and on top of that:

- Collabtive configurations:
   
   - Installed from upstream source code to /var/www/collabtive

- SSL support out of the box.
- `PHPMyAdmin`_ administration frontend for MySQL (listening on port
  12322 - uses SSL).
- Postfix MTA (bound to localhost) to allow sending of email (e.g.,
  password recovery).
- Webmin modules for configuring Apache2, PHP, MySQL and Postfix.

Credentials *(passwords set at first boot)*
-------------------------------------------

- Webmin, SSH, MySQL, phpMyAdmin: username **root**
- Collabtive: username **admin**


.. _Collabtive: http://collabtive.o-dyn.de/
.. _TurnKey Core: http://www.turnkeylinux.org/core
.. _PHPMyAdmin: http://www.phpmyadmin.net
