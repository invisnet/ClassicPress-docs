.. _installation_composer:

========================
Installing with Composer
========================

You can use ``composer`` to install ClassicPress ``v1.0.0-beta1`` and recent nightly builds.

This is a good option if you want to automate more steps of the installation process.

Until ``v1.0.0-beta1`` is available, here is how to install a nightly build using ``composer``:


.. _installation_composer_installation_steps:

Installation steps
------------------

#. Create a composer.json file in your root directory
#. Copy the following code into the ``composer.json`` file::

    {
        "minimum-stability" :"dev",
        "repositories": [
            {
                "type": "composer",
                "url": "https://wpackagist.org"
            },
            {
                "type": "vcs",
                "url": "https://github.com/ClassyBot/ClassicPress-nightly.git"
            }
        ],
        "require": {
            "classicpress/classicpress": "*"
        }
    }

#. In the root directory, run the following command in the command line::

    composer install

#. Create your database
#. In the wp-config.php file, edit following constants: **DB_NAME**, **DB_USER**, **DB_PASSWORD**, **DB_HOST**, and **WP_HOME**. Go to your site home url, and follow standard ClassicPress install steps.


.. _installation_composer_configuration_changes:

Configuration changes
---------------------

A common use of a composer-based installation workflow is to keep core and all plugins and themes up to date in a development environment, and then deploy everything to production at once.

If this is what you have in mind, you’ll probably want to disable auto-updates by adding the following line to your wp-config.php file::

    define( 'WP_AUTO_UPDATE_CORE', false );

It is also a good idea to hide the ``composer.json`` file from the web root so that it is not publicly visible.  If your site is served via Apache then you can use an ``.htaccess`` rule.

Contributions to this page welcome – help us `document this rule <https://forums.classicpress.net/c/team-discussions/documentation-forum>`_ or `implement it automatically <https://github.com/ClassicPress/ClassicPress/issues/218>`_!

