```
           -
         /   \
      /         \
   /   PocketMine  \
/          MP         \
|\     @shoghicp     /|
|.   \           /   .|
| ..     \   /     .. |
|    ..    |    ..    |
|       .. | ..       |
\          |          /
   \       |       /
      \    |    /
         \ | /

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Lesser General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
```

* **Some event data has been ommited, due to future deletion or redundancy**
* Please check PocketMine source code for additional information.
* If a event has the *F* tag, a future update will change it and break plugins using that event.

## PocketMine-MP Handling Events
* A Handling Event is called using the Main API / Server method `mixed handle(string $event, mixed &$data)` or the Main API method `dhandle(string $event, mixed $data)`. The difference is that the dhandle $data is not passed by reference, so normal data will not be modified (be aware of objects).
* Then, handlers created using the Main API / Server method `mixed addHandler(string $event, callable $callable [, integer $priority = 5])` will process that data.
* If a handler returns `false`, PocketMine will stop processing that Handling Event, then return that value to the original caller (where the handle/dhandle method has been called).
* If no handler returns `false`, a normal event will be called.
* All the data can be modified by the handlers, and will be returned by reference except for the dhandle.


### `player.*` Events
#### player.join
* *Sent when a player is connecting, before adding entity or inventory data*
* `object Player`

#### player.quit
* *Sent when a player is disconnecting*
* `object Player`

#### player.armor
* *Sent when a player changes its armor*
* `array( eid => int Entity ID, slot0 => int Item, slot1 => int Item, slot2 => int Item, slot3 => int Item )`

#### player.equipment.change
* *Sent when a player changes its equipment (item in hand)*
* `array( player => object Player, item => object Item )`

#### player.interact
* *Sent when a player (attacks?) with another Entity *
* `array( targetentity => object Entity, entity => object Entity )`

#### player.move
* *Sent when a player has moved*
* `object Entity`

#### player.chat
* *Sent when a player says something (future). Not ran when calling a command*
* `array( player => object Player, message => string Message )`

#### player.pickup *F*
* *Sent when a player gets a dropped item*
* `array( eid => int Entity ID, entity => object Entity, block => int Block, meta => int Metadata, target => Entity ID )`

#### player.death 
* *Sent when a player dies, contains the cause*
* `array( name => string Name, cause => string Cause )`

#### player.block.touch
* *Sent when a player tries to break/place/activate a block, before any check*
* `array( type => string Type, player => object Player, target => object Block, item => object Item [, block => object Block] )`

#### player.block.break
* *Sent when a player tries to break a block, after break checks*
* `array(player => object Player, target => object Block, item => object Item)`

#### player.block.activate
* *Sent when a player tries to activate some block using a tool*
* `array(player => object Player, block => object Block, target => object Block, item => object Item)`

#### player.block.place
* *Sent when a player tries to place a block, after place checks*
* `array(player => object Player, block => object Block, target => object Block, item => object Item)`


## PocketMine-MP Events