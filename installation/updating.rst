.. _installation_updating:

=====================
Updating ClassicPress
=====================

If you’ve previously installed ClassicPress ``1.0.0-alpha1``, a nightly build, or used the migration plugin to switch from WordPress, then you’ll need to follow the manual update process in order to update ClassicPress to the latest version.

Once you get to ``1.0.0-beta1``, the ClassicPress automatic update mechanism will take over and prompt you to keep your site updated.

Updating ClassicPress manually
------------------------------

#. **Back up your site files and database.** This is especially important when you are updating files by hand.
#. Download the latest ClassicPress zip file from our `GitHub releases page <https://github.com/ClassicPress/ClassicPress-release/releases>`_.
#. Unzip the file on your local computer.
#. On your local computer, remove the ``wp-config-sample.php`` file and remove the entire ``wp-content`` folder.
#. Upload what’s left over to your server, replacing the existing files (using either SSH or an application like `CyberDuck <https://cyberduck.io/download/>`_ or `FileZilla <https://filezilla-project.org/>`_).
#. Visit your newly upgraded ClassicPress site.

You may also want to have a look at the corresponding WordPress update page.  These instructions are mostly still relevant to ClassicPress, and there are some helpful tips there: `https://codex.wordpress.org/Updating_WordPress#Manual_Update <https://codex.wordpress.org/Updating_WordPress#Manual_Update>`_

Updating ClassicPress automatically
-----------------------------------

This will be available soon, starting with the upcoming ``1.0.0-beta1`` release!

