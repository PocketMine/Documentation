.. _require:

Requirements
============
PocketMine-MP.phar, the main component, is needed to run PocketMine-MP. 
PocketMine-MP requires a few extra extensions because of that you need custom build PHP binaries. 
We precomiled a few binaries. 
If you have problems you could try to compile PHP with our `compile script from GitHub <https://github.com/PocketMine/php-build-scripts/blob/master/compile.sh>`_. 
Got problems? `Contact us! <http://pocketmine-mp.readthedocs.org/en/latest/intro.html#contact-and-support>`_

PocketMine-MP Installers
------------------------
Windows installer
+++++++++++++++++
Download the installer from `SourceForge <http://sourceforge.net/projects/pocketmine/files/windows/dev/>`_ and start it.

Linux/MacOS
+++++++++++
Use one of the following urls with ``curl`` or ``wget`` to install PocketMine-MP.

.. code-block:: sh

	http://get.pocketmine.net/
	https://raw.githubusercontent.com/PocketMine/php-build-scripts/master/installer.sh


Replace <URL> with a url from above and channel with ``development`` or ``beta``.

.. code-block:: sh

	curl -sL <URL> | bash -s - -v <CHANNEL>
	wget -q -O - <URL> | bash -s - -v <CHANNEL>


.. warning::

    It is recommended to run it as a normal user as it doesn't need further permissions.
    Don't run the installer as root, this is discouraged.


PocketMine-MP.phar
------------------
* `Jenkins <http://jenkins.pocketmine.net/job/PocketMine-MP/promotion/>`_
* `GitHub <https://github.com/PocketMine/PocketMine-MP/releases>`_

Custom PHP binaries
-------------------
* `Windows <PHP-Windows_>`_
* `MacOS <PHP-SourceForge_>`_
* `CentOS <PHP-SourceForge_>`_
* `Linux <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
* `Linux ARM <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
* `Android <PHP-SourceForge_>`_ or `Jenkins <PHP-Jenkins_>`_
* `Raspbian <PHP-SourceForge_>`_

Third-party Libraries/Protocols Used
------------------------------------
* `PHP Sockets <http://php.net/manual/en/book.sockets.php>`_
* `PHP SQLite3 <http://php.net/manual/en/book.sqlite3.php>`_
* `PHP BCMath <http://php.net/manual/en/book.bc.php>`_
* `PHP pthreads <http://pthreads.org/>`_  by `krakjoe <https://github.com/krakjoe>`_ : Threading for PHP - Share Nothing, Do Everything.
* `PHP YAML <https://code.google.com/p/php-yaml/>`_ by Bryan Davis: The Yaml PHP Extension provides a wrapper to the LibYAML library.
* `LibYAML <http://pyyaml.org/wiki/LibYAML>`_  by Kirill Simonov: A YAML 1.1 parser and emitter written in C.
* `cURL <http://curl.haxx.se/>`_ : cURL is a command line tool for transferring data with URL syntax
* `Zlib <http://www.zlib.net/>`_ : A Massively Spiffy Yet Delicately Unobtrusive Compression Library
* `Source RCON Protocol <https://developer.valvesoftware.com/wiki/Source_RCON_Protocol>`_
* `UT3 Query Protocol <http://wiki.unrealadmin.org/UT3_query_protocol>`_

.. _PHP-Windows: http://sourceforge.net/projects/pocketmine/files/windows/dev/
.. _PHP-SourceForge: http://sourceforge.net/projects/pocketmine/files/builds/
.. _PHP-Jenkins: http://jenkins.pocketmine.net/
.. _PM-Stable: https://github.com/PocketMine/PocketMine-MP/releases
.. _PM-Dev: http://jenkins.pocketmine.net/job/PocketMine-MP/
