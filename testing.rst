.. _testing:

====================
Testing ClassicPress
====================


.. _testing_classicpress_is_focused_on_quality:

ClassicPress is focused on quality
----------------------------------

Our Quality Assurance (QA) team focuses on testing and software quality, as well as making sure any bugs get in front of the right people so they can be fixed.

Continuous QA is crucially important in software development because it helps to ensure that any change or update will keep the quality of the software and avoid any new defects or bugs.  Software bugs and defects can have a huge negative impact on the businesses/people that use the software.


.. _testing_how_can_i_help_the_qa_team:

How can I help the QA Team?
---------------------------

We will need all the help we can get to cover all the necessary testing scenarios.

`We’ve released ClassicPress 1.0.0-alpha1 <https://www.classicpress.net/download/>`_ (the first official release) and we need help testing new installs of ClassicPress using this version.

We’ve also released the `migration plugin <https://github.com/ClassicPress/ClassicPress-Migration-Plugin>`_ that will convert a WordPress installation into a ClassicPress installation, and we need help testing that too.

To install ClassicPress using either of these methods, see the :ref:`installation` page.

For a suggested list of testing scenarios, see the :ref:`testing_scenarios` page.

.. toctree::
   :hidden:

   testing/scenarios

To find out more, `join our Slack group <https://www.classicpress.net/join-slack/>`_ and introduce yourself in the `#testing <https://classicpress.slack.com/messages/testing>`_ channel. If for some reason you can’t join the Slack group, you can send us an email to `ClassicPress QA <qa@classicpress.net>`_, but it’s easier for us to coordinate our work on Slack.


.. _testing_testing_process_and_requirements:

Testing process and requirements
--------------------------------

You will need a computer to perform the testing, and of course some free time. Even a few minutes to perform a fresh install or a migration from WordPress to ClassicPress can help.

You should test in new installs or existing site installs that aren’t in production and aren’t important in case something goes wrong.  And of course, **always make a backup of your site files and database first!**


.. _testing_reporting_bugs:

Reporting bugs
--------------

Any bugs that are found can be reported on the GitHub project pages.

You can report bugs in ClassicPress itself `on the ClassicPress GitHub repository <https://github.com/ClassicPress/ClassicPress/issues/new>`_.

You can report bugs related to the ClassicPress migration plugin `on the GitHub repository for the plugin <https://github.com/ClassicPress/ClassicPress-Migration-Plugin/issues/new>`_.

We are happy to help you through the process of reporting a bug as well, just send us a note on `Slack <https://www.classicpress.net/join-slack/>`_ or `email <qa@classicpress.net>`_.


.. _testing_manual_and_automated_testing:

Manual and automated testing
----------------------------

There are two main types of software testing that can be done. One is **manual testing** done by real people and the other is **automated testing** that is performed by computers.

The idea is to have always a mix of both kinds of testing to increase and maintain ClassicPress software quality.

ClassicPress core has an extensive PHP and JavaScript **automated test suite**, which is based on the WordPress automated test suite.  This test suite runs against the ClassicPress code every time any change is made, and the tests are required to pass before the change can be merged.

New code or logic introduced into ClassicPress or its plugins should also have automated tests.

For more information see the `WordPress automated testing handbook <https://make.wordpress.org/core/handbook/testing/automated-testing/>`_ – most of the same information applies to ClassicPress.

