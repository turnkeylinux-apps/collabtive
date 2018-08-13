Collabtive - Open Source Project Management
===========================================

`Collabtive`_ is web-based project management software intended for
small to medium-sizes businesses and freelancers. It is an open Source
alternative to proprietary tools like Basecamp. Key features include
tracking of projects, milestones, and tasks, importing from Basecamp,
timetracking and reporting.

This appliance includes all the standard features in `TurnKey Core`_,
and on top of that:

- Collabtive configurations:
   
   - Installed from upstream source code to /var/www/collabtive

     **Security note**: Updates to Collabtive may require supervision so
     they **ARE NOT** configured to install automatically. See below for
     updating Collabtive.

- SSL support out of the box.
- `Adminer`_ administration frontend for MySQL (listening on port
  12322 - uses SSL).
- Postfix MTA (bound to localhost) to allow sending of email (e.g.,
  password recovery).
- Webmin modules for configuring Apache2, PHP, MySQL and Postfix.

Supervised Manual Collabtive Update
-----------------------------------

Always ensure that you have a current and tested backup before performing an
upgrade. Ideally also do a test upgrade proceedure on a development server,
before updating your production server.

  1. Download the latest version of Collabtive::

    cd /var/www
    URL=https://sourceforge.net/projects/collabtive/files/latest/download
    wget $URL -O collabtive.zip

  2. Move the current config::

    mv /var/www/collabtive/config /var/www/collabtive/config.orig

  3. Unpack the Collabtive archive - replacing all existing files::

    unzip collabtive.zip -d /var/www/collabtive

  4. Move original config back into place::

    cp -R /var/www/collabtive/config.orig/* /var/www/collabtive/config/

  5. Ensure directory is owned by the webser user (www-data)::

    chown -r www-data:www-data /var/www/collabtive

  6. Point your browser to update.php and follow the in browser instructions.

  7. Delete install.php and update.php from your server.

Credentials *(passwords set at first boot)*
-------------------------------------------

- Webmin, SSH, MySQL: username **root**
- Adminer: username **adminer**
- Collabtive: username **admin**


.. _Collabtive: http://collabtive.o-dyn.de/
.. _TurnKey Core: https://www.turnkeylinux.org/core
.. _Adminer: https://www.adminer.org/
