Commands
--------

.. code-block:: yaml

    name: Example
    main: Example\Example
    version: 1.0.0
    api: 1.12.0

    commands:
     example1:
      description: "Example1 command"
      usage: "/example1"
     example2:
      descroption "Example2 command with arguments"
      usage: "/example2 <args>"


.. code-block:: php
    :linenos:

    <?php
    namespace Example;

    use pocketmine\plugin\PluginBase;
    use pocketmine\command\Command;
    use pocketmine\command\CommandSender;

    class Example extends PluginBase{

        public function onCommand(CommandSender $sender, Command $command, $label, array $args) {
            switch($command->getName()) {
                case "example1":
                    // do stuff
                    return true;
                case "example2":
                    if (count($args) == 0 ){
                        return false;
                    }
                    var_dump($args); // do stuff
                    return true;
            }
        }
    }
