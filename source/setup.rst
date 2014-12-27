.. _setup:

Installation
============

Installing on Windows
---------------------
Download the latest version from `sourceforge <http://sourceforge.net/projects/pocketmine/files/windows/dev/>`_.
Use the installer to install PocketMine-MP.
The installer may have an outdated version of PocketMine-MP. 
You can download the latest .phar from `github <https://github.com/PocketMine/PocketMine-MP/releases>`_ 
or `Jenkins <http://jenkins.pocketmine.net/job/PocketMine-MP/promotion/>`_.

.. warning::
    If the provided x64 binary does not work then try the x86 binary!

Installing on Linux
-------------------
Open the terminal

Navigate where you want to install/update PocketMine-MP. You can move around using ``cd [directory]``, and create directories using ``mkdir [name]``

.. code-block:: sh

	~/ $ mkdir PocketMine-MP			# make new directory
	~/ $ cd PocketMine-MP				# change to directory
	PocketMine-MP/ $ 

Run the following code. It will download PocketMine-MP, download the PHP binaries or compile it if binaries are not available.

.. code-block:: sh

	PocketMine-MP/ $ curl -sL \
	https://raw.githubusercontent.com/PocketMine/php-build-scripts/master/installer.sh \
	 | bash -s - -v development

	[INFO] Found PocketMine-MP Alpha_1.4dev (build 289) using API 1.1.0
	[INFO] This development build was released on Thu Jul 17 21:31:35 CEST 2014
	[INFO] Installing/updating PocketMine-MP on directory ./
	[1/3] Cleaning...
	[2/3] Downloading PocketMine-MP Alpha_1.4dev-289 phar... done!
	[3/3] Obtaining PHP: detecting if build is available...
	[3/3] Linux 64-bit PHP build available, downloading PHP_5.5.14_x86-64_Linux.tar.gz... checking... regenerating php.ini... done
	[INFO] Everything done! Run ./start.sh to start PocketMine-MP

Installing on OS X
------------------
Open the Terminal.app. (Applications -> Utilities -> Terminal)

Navigate where you want to install/update PocketMine-MP. You can move around using ``cd [directory]``, and create directories using ``mkdir [name]``

.. code-block:: sh

	~/ $ mkdir PocketMine-MP			# make new directory
	~/ $ cd PocketMine-MP				# change to directory
	PocketMine-MP/ $ 

Run the following code. It will download PocketMine-MP, download the PHP binaries or compile it if binaries are not available.

.. code-block:: sh

	PocketMine-MP/ $ curl -sL \
	https://raw.githubusercontent.com/PocketMine/php-build-scripts/master/installer.sh \
	 | bash -s - -v development

	[INFO] Found PocketMine-MP Alpha_1.4dev (build 289) using API 1.1.0
	[INFO] This development build was released on Thu Jul 17 21:31:35 CEST 2014
	[INFO] Installing/updating PocketMine-MP on directory ./
	[1/3] Cleaning...
	[2/3] Downloading PocketMine-MP Alpha_1.4dev-289 phar... done!
	[3/3] Obtaining PHP: detecting if build is available...
	[3/3] MacOS 64-bit PHP build available, downloading PHP_5.5.14_x86-64_MacOS.tar.gz... checking... regenerating php.ini... done
	[INFO] Everything done! Run ./start.sh to start PocketMine-MP


Installing on Android
---------------------
Install `PocketMine-MP for Android <https://play.google.com/store/apps/details?id=net.pocketmine.server>`_

Installing manually
-------------------
Did the installer fail? It's not your taste? YOLO? DIY! 

1. Create a new directory
2. Download PocketMine-MP.phar from `Jenkins <http://jenkins.pocketmine.net/job/PocketMine-MP/promotion/>`_ or `GitHub <https://github.com/PocketMine/PocketMine-MP/releases>`_
3. Rename the .phar to PocketMine-MP.phar
4. Download your flavor PHP binary.
	* `Windows <PHP-Windows_>`_
	* `MacOS <PHP-SourceForge_>`_
	* `CentOS <PHP-SourceForge_>`_
	* `Linux <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
	* `Linux ARM <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
	* `Android <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
	* `Raspbian <PHP-SourceForge_>`_
5. Extract the PHP binary
6. Download the `start.sh <https://raw.githubusercontent.com/PocketMine/PocketMine-MP/master/start.sh>`_
7. Make start.sh executable (chmod +x start.sh)

If you start PocketMine-MP now it will tell you that it failed to load opcache.so.
`Fix it using this <faq.html#failed-loading-opcache-so>`_. Now start PocketMine-MP with ``./start.sh``

.. _PHP-Windows: http://sourceforge.net/projects/pocketmine/files/windows/dev/
.. _PHP-SourceForge: http://sourceforge.net/projects/pocketmine/files/builds/
.. _PHP-Jenkins: http://jenkins.pocketmine.net/
.. _PM-Stable: https://github.com/PocketMine/PocketMine-MP/releases
.. _PM-Dev: http://jenkins.pocketmine.net/job/PocketMine-MP/

