.. _installation:

Installation
============

Installing on Windows
---------------------

Download the latest version from `Bintray <Win-Bintray_>`_.
Use the installer to install PocketMine-MP.
The installer may have an outdated version of PocketMine-MP.
You can download the latest .phar from `GitHub`_ or `Jenkins`_.

.. warning::
    If the provided x64 binary does not work then try the x86 binary.

Installing on Linux/MacOS
-------------------------

Use one of the following urls with ``curl`` or ``wget`` to install PocketMine-MP.

.. code-block:: sh

	https://get.pocketmine.net/
	https://raw.githubusercontent.com/PocketMine/php-build-scripts/master/installer.sh

Replace ``<URL>`` with one from above and ``<VERSION>`` with ``stable``, ``beta``, ``development``.

.. code-block:: sh

	curl -sL <URL> | bash -s - -v <VERSION>
	wget -q -O - <URL> | bash -s - -v <VERSION>

.. code-block:: sh

  [*] Found PocketMine-MP Final_1.5dev (build 1254) using API 1.12.0
  [*] This development build was released on Sat Jun 20 09:45:04 CEST 2015
  [*] Installing/updating PocketMine-MP on directory ./
  [1/3] Cleaning...
  [2/3] Downloading PocketMine-MP Final_1.5dev-1254 phar... done!
  [3/3] Obtaining PHP: detecting if build is available...
  [3/3] MacOS 64-bit PHP build available, downloading PHP_5.6.10_x86-64_MacOS.tar.gz... checking... regenerating php.ini... done
  [*] Everything done! Run ./start.sh to start PocketMine-MP

.. error::

    It is recommended to run it as a **normal user** as it doesn't need further permissions.

    **Do not run the installer as root, this is discouraged**.

Installing on Android
---------------------

Install `PocketMine-MP for Android`_ from the Google play.

Installing manually
-------------------

Did the installer fail? It is not your taste? YOLO? DIY!

Using .phar
~~~~~~~~~~~

1. Create a new directory for PocketMine-MP.
2. Download PocketMine-MP.phar from `GitHub`_ or `Jenkins`_.
3. Rename the .phar to ``PocketMine-MP.phar``.
4. Place it in the PocketMine-MP directory you just created.

Using GitHub
~~~~~~~~~~~~

.. code::

    $ git clone --recursive https://github.com/PocketMine/PocketMine-MP.git PocketMine-MP.git
    Cloning into 'PocketMine-MP.git'...
    remote: Counting objects: 34068, done.
    remote: Compressing objects: 100% (13/13), done.
    remote: Total 34068 (delta 2), reused 0 (delta 0), pack-reused 34055
    Receiving objects: 100% (34068/34068), 9.89 MiB | 1.79 MiB/s, done.
    Resolving deltas: 100% (25602/25602), done.
    Checking connectivity... done.
    Submodule 'src/pocketmine/gui' (https://github.com/PocketMine/PocketMine-MP-GUI.git) registered for path 'src/pocketmine/gui'
    Submodule 'src/raklib' (https://github.com/PocketMine/RakLib.git) registered for path 'src/raklib'
    Submodule 'src/spl' (https://github.com/PocketMine/PocketMine-SPL.git) registered for path 'src/spl'
    Submodule 'tests/TesterPlugin' (https://github.com/PocketMine/TesterPlugin.git) registered for path 'tests/TesterPlugin'
    Cloning into 'src/pocketmine/gui'...
    remote: Counting objects: 26, done.
    remote: Compressing objects: 100% (21/21), done.
    remote: Total 26 (delta 4), reused 26 (delta 4), pack-reused 0
    Unpacking objects: 100% (26/26), done.
    Checking connectivity... done.
    Submodule path 'src/pocketmine/gui': checked out 'b551c3d58ec2fd9fa0f3c92d36fcbaa5c70467f7'
    Cloning into 'src/raklib'...
    remote: Counting objects: 577, done.
    remote: Total 577 (delta 0), reused 0 (delta 0), pack-reused 577
    Receiving objects: 100% (577/577), 141.29 KiB | 0 bytes/s, done.
    Resolving deltas: 100% (432/432), done.
    Checking connectivity... done.
    Submodule path 'src/raklib': checked out '660bdff07d85c0270e57da2a5ce69eff2a87649a'
    Cloning into 'src/spl'...
    remote: Counting objects: 65, done.
    remote: Total 65 (delta 0), reused 0 (delta 0), pack-reused 65
    Unpacking objects: 100% (65/65), done.
    Checking connectivity... done.
    Submodule path 'src/spl': checked out '178d2a38f95d552fa5d91da26edc13a86d8054c6'
    Cloning into 'tests/TesterPlugin'...
    remote: Counting objects: 8, done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 8 (delta 2), reused 1 (delta 1), pack-reused 5
    Unpacking objects: 100% (8/8), done.
    Checking connectivity... done.
    Submodule path 'tests/TesterPlugin': checked out '1a0dec97cc354a0b62b41c007caa6f84885b8263'

Getting PHP and the start script
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Downlad your flavor PHP binary.

   * Windows `Bintray <Bintray_>`_
   * MacOS `Bintray <PHP-Bintray_>`_
   * CentOS `Bintray <PHP-Bintray_>`_
   * Linux `Bintray <PHP-Bintray_>`_ or `Jenkins <PHP-Jenkins_>`_
   * Linux ARM `Bintray <PHP-Bintray_>`_ or `Jenkins <PHP-Jenkins_>`_
   * Android `Bintray <PHP-Bintray_>`_ or `Jenkins <PHP-Jenkins_>`_
   * Raspbian `Bintray <PHP-Bintray_>`_

2. Extract the PHP binary
3. Download the `start.sh <https://raw.githubusercontent.com/PocketMine/PocketMine-MP/master/start.sh>`_
4. Make start.sh executable (chmod +x start.sh)

Starting for the first time
---------------------------

Now you should be able to start PocketMine-MP.
The first time it starts with a set-up wizard,
this can be disabled by running ``./start.sh --no-wizard``.

.. code::

    $ ./start.sh
    [*] PocketMine-MP set-up wizard
    [*] Please select a language:
    English => en
    EspaÃ±ol => es
    ä¸­æ–‡ => zh
    PyccÄ¸Ð¸Ð¹ => ru
    æ—¥æœ¬èªž => ja
    Deutsch => de
    í•œêµ­ì–´ => ko
    Nederlands => nl
    FranÃ§ais => fr
    Italiano => it
    Melayu => ms
    Norsk => no
    Svenska => sv
    Suomi => fi
    TÃ¼rkÃ§e => tr
    [?] Language (en):

PocketMine-MP supports a few other languages.
Fill in the two letters behind the language and press enter.
Is your language not in the list? Add it on `Crowdin`_.

.. code::

    [*] English has been correctly selected.
    Welcome to PocketMine-MP!
    Before starting setting up your new server you have to accept the license.
    PocketMine-MP is licensed under the LGPL License,
    that you can read opening the LICENSE file on this folder.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU Lesser General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    [?] Do you accept the License? (y/N):

Do you accept the `License`_?

.. code::

    [?] Do you want to skip the set-up wizard? (y/N):

You can skip the wizard from here and start the server with the default settings or continue.

.. code::

    [*] You are going to set up your server now.
    [*] If you don't want to change the default value, just press Enter.
    [*] You can edit them later on the server.properties file.
    [?] Give a name to your server (Minecraft: PE Server):
    [*] Do not change the default port value if this is your first server.
    [?] Server port (19132):
    [*] The RAM is the maximum amount of memory PocketMine-MP will use. A value of 128-256 MB is recommended
    [?] Server RAM in MB (256):
    [*] Choose between Creative (1) or Survival (0)
    [?] Default Game mode: (0):
    [?] Max. online players (20):
    [*] The spawn protection disallows placing/breaking blocks in the spawn zone except for OPs
    [?] Enable spawn protection? (Y/n):
    [*] An OP is the player admin of the server. OPs can run more commands than normal players
    [?] OP player name (example, your game name):
    [!] You will be able to add an OP user later using /op <player>
    [*] The white-list only allows players in it to join.
    [?] Do you want to enable the white-list? (y/N):
    [!] Query is a protocol used by different tools to get information of your server and players logged in.
    [!] If you disable it, you won't be able to use server lists.
    [?] Do you want to disable Query? (y/N):
    [*] RCON is a protocol to remote connect with the server console using a password.
    [?] Do you want to enable RCON? (y/N):
    [*] Getting your external IP and internal IP
    [!] Your external IP is 87.212.35.149. You may have to port-forward to your internal IP 192.168.0.150
    [!] Be sure to check it, if you have to forward and you skip that, no external players will be able to join. [Press Enter]
    [*] You have finished the set-up wizard correctly
    [*] Check the Plugin Repository to add new features, minigames, or advanced protection to your server
    [*] PocketMine-MP will now start. Type /help to view the list of available commands.

    [Server thread/INFO]: Loading pocketmine.yml...
    [Server thread/INFO]: Loading server properties...
    [Server thread/INFO]: Selected English (eng) as the base language
    [Server thread/INFO]: Starting Minecraft: PE server version v0.11.0 alpha
    [Server thread/NOTICE]: The memory-limit setting has been deprecated.
    [Server thread/NOTICE]: There are new memory settings on pocketmine.yml to tune memory and events.
    [Server thread/NOTICE]: You can also reduce the amount of threads and chunks loaded control the memory usage.
    [Server thread/INFO]: Opening server on 0.0.0.0:19132
    [Server thread/INFO]: This server is running PocketMine-MP version 1.5dev-1254 "活発(Kappatsu)フグ(Fugu)" (API 1.12.0)
    [Server thread/INFO]: PocketMine-MP is distributed under the LGPL License
    [Server thread/INFO]: Preparing level "world"
    [Server thread/INFO]: Starting GS4 status listener
    [Server thread/INFO]: Setting query port to 19132
    [Server thread/INFO]: Query running on 0.0.0.0:19132
    [Server thread/INFO]: Default game type: Survival Mode
    [Server thread/INFO]: Done (19.485s)! For help, type "help" or "?"

The server should have started now and you should be able to join.


.. _Win-Bintray: https://bintray.com/pocketmine/PocketMine/Windows-PHP-Binaries/view#files
.. _GitHub: https://github.com/PocketMine/PocketMine-MP/releases
.. _Jenkins: http://jenkins.pocketmine.net/job/PocketMine-MP/promotion/
.. _PHP-Bintray: https://bintray.com/pocketmine/PocketMine/Unix-PHP-Binaries/view#files
.. _PHP-Jenkins: http://jenkins.pocketmine.net/
.. _PM-Stable: https://github.com/PocketMine/PocketMine-MP/releases
.. _PM-Dev: http://jenkins.pocketmine.net/job/PocketMine-MP/
.. _PocketMine-MP for Android: https://play.google.com/store/apps/details?id=net.pocketmine.server
.. _Crowdin: http://translate.pocketmine.net
.. _License: https://github.com/PocketMine/PocketMine-MP/blob/master/LICENSE
