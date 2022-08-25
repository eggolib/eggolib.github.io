---
title: Action on Block Place (Power Type)
date: 2022-07-13
search:
    boost: 2
---

#   Action on Block Place

**[Power Type]**

Executes an action upon placing a block.

Type ID: `eggolib:action_on_block_place`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the player upon placing a block.
`held_item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the item the player has used to place a block.
`result_item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the item that will be given to the player upon placing a block.
`place_to_action` | **[Block Action Type]** | *optional* | If specified, this action will be executed at the position of the block the player has placed.
`place_on_action` | **[Block Action Type]** | *optional* | If specified, this action will be executed on the block the player placed a block on.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only execute the specified actions if the item the player has used to place a block fulfills this condition.
`place_to_condition` | **[Block Condition Type]** | *optional* | If specified, only execute the specified actions if the old block at the position of the new block the player has placed fulfills this condition.
`place_on_condition` | **[Block Condition Type]** | *optional* | If specified, only execute the specified actions if the block the player placed a block on fulfills this condition.
`directions` | **[Array]** of **[Strings]** | `["up", "down", "north", "south", "east", "west"]` | Determines if the specified actions should be executed if the player has placed a block at the specified side(s) of a block.
`hands` | **[Array]** of **[Strings]** | `["main_hand", "off_hand"]` | Determines if the specified actions should be executed if the player has attempted to place a block using the specified hand(s).
`result_stack` | **[Item Stack]** | *optional* | If specified, this item will be given to the player upon placing a block.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:action_on_block_place",
        "entity_action": {
            "type": "apoli:execute_command",
            "command": "me placed a Dragon Egg!"
        },
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:dragon_egg"
            }
        }
    }
    ```

    This example will announce to all players that the player that has the power has placed a Dragon Egg if the player in question did place a Dragon Egg.

=== "Example #2"

    ``` json
    {
        "type": "eggolib:action_on_block_place",
        "entity_action": {
            "type": "apoli:heal",
            "amount": 2
        },
        "place_to_action": {
            "type": "apoli:set_block",
            "block": "minecraft:air"
        },
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "tag": "minecraft:wool"
            }
        },
        "place_on_condition": {
            "type": "apoli:block",
            "block": "minecraft:diamond_block"
        },
        "directions": [
            "up"
        ]
    }
    ```

    This example will heal the player that has the power if the player in question places a Wool block on top of a Diamond Block.



[Power Type]: ../power_types.md
[Entity Action Type]: ../entity_action_types.md
[Item Action Type]: https://origins.readthedocs.io/en/latest/types/item_action_types
[Block Action Type]: ../block_action_types.md
[Item Condition Type]: ../item_condition_types.md
[Block Condition Type]: ../block_condition_types.md
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Strings]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Item Stack]: https://origins.readthedocs.io/en/latest/types/data_types/item_stack
