.. _installation:

=======================
Installing ClassicPress
=======================

.. _installation_how_to_do_a_fresh_install_of_classicpress:

How to do a fresh install of ClassicPress
-----------------------------------------

Installing ClassicPress is the first step of your ClassicPress journey. The process in itself will typically take you about five minutes if you are experienced with installing similar web CMS’s. However, should this be your first time installing a CMS on your server, don’t worry. We’ll take you through each of the steps in detail – and if there’s any problem along the way, don’t hesitate to call on the community.

Before you start, you’ll need a few things in order to make the installation process as smooth as possible.  We recommend collecting this information ahead of time.


.. _installation_server_or_shared_hosting_environment:

Server or shared hosting environment
------------------------------------

This is a place to store your site’s files and content so that the site is visible to the world.  The hosting environment usually comes with a domain name.

If you don’t have this yet, we recommend taking a look at `SiteGround <https://www.siteground.com/>`_ – their basic plan is more than sufficient to run ClassicPress.

You can also install ClassicPress on your local computer.  A site made this way will not be accessible to the public, but it’s great for trying out ClassicPress and its features.  In order to do this, you’ll need to install a *web server program* like `Local by Flywheel <https://local.getflywheel.com/>`_.


.. _installation_program_to_copy_files_to_the_server:

Program to copy files to the server
-----------------------------------

If you’re installing ClassicPress on a hosting environment or another remote server, you’ll need to use a program to copy files back and forth.  We recommend getting an `SSH <https://en.wikipedia.org/wiki/Secure_Shell>`_ account set up with your hosting provider and using this account to copy files via `SFTP <https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol>`_.  (`FTP <https://en.wikipedia.org/wiki/File_Transfer_Protocol>`_) is also an option, but we do not recommend it because it *does not use a secure, encrypted connection* to transfer files.)

`FileZilla <https://filezilla-project.org/>`_ is one program that can copy files to and from almost any server or shared hosting environment.  `CyberDuck <https://cyberduck.io/download/>`_ is another.


.. installation_mysql_or_mariadb_database:

MySQL or MariaDB database
-------------------------

Usually your hosting provider will set this up for you, and you’ll need the *database name*, *username* and *password* for the database.


.. installation_installation_steps:

Installation steps
------------------

Once you have all of the above requirements met, you should be able to proceed with the installation.

#. Download the zip file for ClassicPress from our GitHub releases page (or use this direct link to the 1.0.0-beta1 release).
#. Unzip the file on your local computer.
#. Upload the unzipped folder to your server (using either SFTP or FTP).
#. Create a database for ClassicPress (contact your web host if you aren’t sure how to do this).
#. Run the ClassicPress Install by going to the domain name associated with your site.
#. Fill in the required information requested, including the database information set up in Step 4.


.. _installation_installing_with_composer:

Installing with Composer
------------------------

You can use composer to install ClassicPress ``v1.0.0-beta1`` and recent nightly builds.

This is a good option if you want to automate more steps of the installation process.  For more details, visit the :ref:`installation_composer` page.

.. toctree::
   :hidden:

   installation/composer


.. _how_to_migrate_from_wordpress_to_classicpress:

How to migrate from WordPress to ClassicPress
---------------------------------------------

Migrating from WordPress to ClassicPress does not touch your site content (posts, pages, CPTs, themes, plugins, uploads), anything else in your database, `wp-config.php`, `.htaccess`, etc.  It only replaces the core WordPress files, most of which are in the `wp-admin` and `wp-includes` directories.

To migrate a current WordPress site to ClassicPress, follow these steps:

#. **PLEASE NOTE:** As ClassicPress is currently in the alpha release stage, we do not recommend that you switch a live production site to ClassicPress. Please also ensure any known conflicting plugins are *deactivated* (see list below).
#. Backup the current site — you can do a manual backup in your hosting panel and export the database or you can use some of the recognized backup plugins like `BackUpWordPress <https://wordpress.org/plugins/backupwordpress/>`_ to do this.
#. Download the ClassicPress migration plugin from `the plugin’s GitHub releases page <https://github.com/ClassicPress/ClassicPress-Migration-Plugin/releases>`_ (or use this `direct link to the plugin’s 0.2.0 release <https://github.com/ClassicPress/ClassicPress-Migration-Plugin/releases/download/0.2.0/upgrade-to-classicpress.zip>`_).
#. Upload the plugin using the WordPress plugins section of your site.
#. Activate the ClassicPress migration plugin.
#. Go to the settings of the ClassicPress migration plugin at Tools -> Switch to ClassicPress.
#. To proceed with the switch it is necessary that all pre-flight checks succeed, with a green check mark.
#. Press the **Switch this site to ClassicPress now!** button.
#. The migration process may take a few minutes depending on your hosting provider, so go grab some water or a beverage of your choice 🙂
#. When the process is finished, you should see the ClassicPress About screen.

We don’t currently support migrating multisite WP installations to ClassicPress, but it’s planned for the future.  In the meantime, if you’re willing to try, you can make some manual code edits to the plugin, or you can try a manual migration (see below).

We would love your help with getting multisite migrations implemented.  For more information, see `the GitHub issue for multisite migration <https://github.com/ClassicPress/ClassicPress-Migration-Plugin/issues/29>`_.

If you have any problems, please `join our Slack group <https://www.classicpress.net/join-slack/>`_ and ask in the `**#support** <https://classicpress.slack.com/messages/support>`_ channel.


.. installation_migrating_to_classicpress_without_using_the_plugin:

Migrating to ClassicPress without using the plugin
--------------------------------------------------

Again, **DO NOT DO THIS ON A PRODUCTION ENVIRONMENT**.

#. **Back up your site files and database.**  This is especially important when you are migrating files by hand.
#. Download the latest ClassicPress zip file from our `GitHub releases page <https://github.com/ClassicPress/ClassicPress-release/releases>`_.
#. Unzip the file on your local computer.
#. On your local computer, remove the `wp-config-sample.php` file and remove the entire `wp-content` folder.
#. Upload what’s left over to your server, replacing the existing files (using either SSH or an application like `CyberDuck <https://cyberduck.io/download/>`_ or `FileZilla <https://filezilla-project.org/>`_).
#. Visit your new ClassicPress site.


.. _installation_plugin_conflicts:

Plugin conflicts
----------------

The following plugins have been reported to conflict with the ClassicPress migration plugin or with ClassicPress itself:

#. **WP Config File Editor** – reported to conflict with the migration process.
#. **Disable WP Core Updates Advance** – reported to conflict with the migration process.
#. **WordFence** – WordFence doesn’t know how to scan ClassicPress core files for changes yet.  After installing ClassicPress, uncheck this option: “*Scan Options → General Options → Scan core files against repository versions for changes*”.  There will also be a few more errors if you have the “*Scan wp-admin and wp-includes for files not bundled with WordPress*” option enabled, because ClassicPress has added new files.  Currently this is normal and expected.

.. _installation_updating_classicpress:

Updating ClassicPress
---------------------

.. toctree::
   :hidden:

   installation/updating

For more information about updating ClassicPress to the latest version, see the :ref:`installation_updating` page.
