Plugins
=======
**PocketMine is extendable!**

Plugins are available on the `PocketMine website <http://forums.pocketmine.net/plugins/>`_ or you can make your own plugin.

Below is an skeleton with the minimal needed directories, files and content.

.. note::
    To run plugins from source or `create .phar files`_ you need `DevTools <http://jenkins.pocketmine.net/job/DevTools%20Plugin/>`_.

Basic plugin structure
----------------------

.. contents::
	:local:
	:depth: 3

Directories
+++++++++++
Make sure your base structure looks like this

.. code-block:: sh

	PocketMine-MP
	└── plugins
	    └── Example
    	        ├── plugin.yml
    	        └── src
                    └── Example
                        └── Example.php

	5 directories, 2 files

plugin.yml
++++++++++
This file is required in a plugin. It contains the information used by PocketMine-MP to load this plugin. It's in YAML format (you will use this format for plugin configurations). It has four required fields: name, version, api and main. Each one of these fields (and all the optional ones) are described on the plugin.yml page. Be sure that it is named exactly plugin.yml.

======= ====================================================================================
field   data
======= ====================================================================================
name    The name for your plugin
main    The namespace and classname pointing to your main plugin class. It is case sensitive
version The version string of your plugin
api     Minimal PocketMine-MP API version required for your plugin (`current <https://github.com/PocketMine/PocketMine-MP/search?utf8=✓&q=filename%3APocketMine.php+%22const+API_VERSION%22&type=Code>`_)
======= ====================================================================================

.. code-block:: yaml

	name: Example
	main: Example\Example
	version: 1.0.0
	api: 1.12.0

Example.php
+++++++++++
Now, create the main class file, that will include the PluginBase Class that starts the plugin. You can name it whatever you want, but a common way to name it is like the plugin name or Main.

.. code-block:: php

	<?php

	namespace Example;

	use pocketmine\plugin\PluginBase;

	class Example extends PluginBase{

		public function onLoad(){
			$this->getLogger()->info("onLoad() has been called!");
		}

		public function onEnable(){
			$this->getLogger()->info("onEnable() has been called!");
		}

		public function onDisable(){
			$this->getLogger()->info("onDisable() has been called!");
		}
	}

Create .phar files
------------------

The easiest way to release a plugin is in .phar format.
To create a .phar you need `DevTools <http://jenkins.pocketmine.net/job/DevTools%20Plugin/>`_.

1. Start PocketMine-MP
2. Make sure the plugin is loaded. Look for ``Loading source plugin <plugin name>``
3. Run ``makeplugin <plugin name>``

The ``<plugin name>`` should be the same as the name in plugin.yml.

.. code-block:: sh

  # Output for the Example plugin
  [Server thread/INFO]: Loading source plugin Example v1.0.0
  [Server thread/INFO]: [Example] onLoad() has been called!
  [Server thread/INFO]: Enabling Example v1.0.0
  [Server thread/INFO]: [Example] onEnable() has been called!
  makeplugin Example
  [Server thread/INFO]: [DevTools] Adding plugin.yml
  [Server thread/INFO]: [DevTools] Adding src/Example/Example.php
  [Server thread/INFO]: Phar plugin Example v1.0.0 has been created on /Pocketmine-MP/dev/plugins/DevTools//Example_v1.0.0.phar

More examples
-------------

.. toctree::
    :glob:

    pluginexamples/*


Resources
---------

* `PocketMine-MP Stable API Documentation <http://docs.pocketmine.net/>`_
* `PocketMine-MP Development API Documentation <http://jenkins.pocketmine.net/job/PocketMine-MP-doc/doxygen/>`_
* `Plugin Development forum <https://forums.pocketmine.net/forums/development/>`_
