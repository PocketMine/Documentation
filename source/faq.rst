.. _faq:

FAQ - Frequently Asked Questions
================================

.. contents::
	:local:
	:depth: 2

Installation
------------

How do I install PHP? / How do I install this Server?
+++++++++++++++++++++++++++++++++++++++++++++++++++++
Check the installation instructions on the :ref:`installation <setup>` page.

Can't install as user root
++++++++++++++++++++++++++
.. warning::

    This script is running as root, this is discouraged.
    It is recommended to run it as a normal user as it doesn't need further permissions.

We recommend you to install PocketMine-MP as a normal user, not as root. 
Create one if you don't have one.

.. code-block:: sh

    useradd -d /home/pocketmine -m pocketmine
    passwd pocketmine

Failed loading opcache.so
+++++++++++++++++++++++++
This will fail when you did not use the installer. This can be fixed with a single command.

.. code-block:: sh

	sed "s/^zend_extension=.*opcache.so/zend_extension=$(find $(pwd) -name opcache.so | sed 's/\//\\\//g')/g" \
	bin/php5/bin/php.ini | tee bin/php5/bin/php.ini

or manually editing the bin/php5/bin/php.ini file.

1. Find opcache.so in the bin directory
2. Edit bin/php5/bin/php.ini and replace everything after "zend_extensions=" with the full path of opcache.so

Playing
-------

Can PC Minecraft clients connect to this server
+++++++++++++++++++++++++++++++++++++++++++++++
No

Plugins
-------

How do I install Plugins
++++++++++++++++++++++++
Download the ``.phar`` file and move it to the ``plugins`` folder. Reload the server by typing 'reload' on the terminal console.

Can i use .php files
++++++++++++++++++++
Yes, but only when the `DevTools <http://forums.pocketmine.net/plugins/devtools.515/>`_ plugin is installed and the plugin/PocketMine API versions are both the same

Connecting
----------

How do I connect to the server?
+++++++++++++++++++++++++++++++
* Tap Play -> Edit -> External, then fill in the server details
* If it is in your local network, you will find it highlighted on the play menu, without needing to add it

Can other users connect to my server
++++++++++++++++++++++++++++++++++++
Users on the same network are able to join the server. If you want other people from outside your own network to be able to join then you need to port-forward

Do I have to open ports?
++++++++++++++++++++++++
If you have a firewall setup then you need to allow access to ``UDP port 19132``

.. note::

	Do you want to use **RCON** then ``TCP port 19132`` also needs access.

Do I have to configure port forwarding?
+++++++++++++++++++++++++++++++++++++++++++
This is only needed when you want people from outside your network to connect. 
Check `portforward.com <http://portforward.com/english/routers/port_forwarding/routerindex.htm>`_
or use `Google <http://www.google.com>`_ to find the instructions. Use the brand and type of your router as keywords.

.. note::

	* UDP port: 19132 for PocketMine and Query
	* TCP port: 19132 for RCON

.. warning::

    * Forward the ports to the IP of your server
