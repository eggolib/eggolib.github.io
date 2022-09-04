---
title: Prevent Block Place (Power Type)
date: 2022-07-13
search:
    boost: 2
---

#   Prevent Block Place

[**Power Type**][1]

Prevents the player that has the power from placing a block.

Type ID: `eggolib:prevent_block_place`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed on the player upon attempting to place a block.
`held_item_action` | [**Item Action Type**][3] | *optional* | If specified, this action will be executed on the item the player has used to place a block.
`result_item_action` | [**Item Action Type**][3] | *optional* | If specified, this action will be executed on the item that will be given to the player upon placing a block.
`place_to_action` | [**Block Action Type**][4] | *optional* | If specified, this action will be executed at the position of the block the player has attempted to place.
`place_on_action` | [**Block Action Type**][4] | *optional* | If specified, this action will be executed on the block the player attempted to place a block on.
`item_condition` | [**Item Condition Type**][5] | *optional* | If specified, only execute the specified actions if the item the player has used to place a block fulfills this condition.
`place_to_condition` | [**Block Condition Type**][6] | *optional* | If specified, only execute the specified actions if the old block at the position of the new block the player has attempted to place fulfills this condition.
`place_on_condition` | [**Block Condition Type**][6] | *optional* | If specified, only execute the specified actions if the block the player has attempted to place a block on fulfills this condition.
`directions` | [**Array**][7] of [**Strings**][8] | `["up", "down", "north", "south", "east", "west"]` | Determines if the specified actions should be executed if the player has attempted to place a block at the specified side(s) of a block.
`hands` | [**Array**][7] of [**Strings**][8] | `["main_hand", "off_hand"]` | Determines if the specified actions should be executed if the player has attempted to place a block using the specified hand(s).
`result_stack` | [**Item Stack**][9] | *optional* | If specified, this item will be given to the player upon attempting to place a block.


### Examples

=== "Example #1"

    ```json
    {
        "type": "eggolib:prevent_block_place",
        "place_to_condition": {
            "type": "apoli:fluid",
            "fluid_condition": {
                "type": "apoli:in_tag",
                "tag": "minecraft:water"
            }
        }
    }
    ```

    This example will prevent the player that has the power from placing a block if there's a Water fluid at where the block is supposed to be placed to.

=== "Example #2"

    ``` json
    {
        "type": "eggolib:prevent_block_place",
        "entity_action": {
            "type": "apoli:execute_command",
            "command": "title @s actionbar {\"text\": \"Can't place a block there!\", \"color\": \"red\"}"
        },
        "place_on_condition": {
            "type": "apoli:block",
            "block": "minecraft:farmland"
        },
        "directions": [
            "up"
        ]
    }
    ```
    This example will prevent the player that has the power from placing a block on top of a Farmland block.



[1]: ../power_types.md
[2]: ../entity_action_types.md 
[3]: https://origins.readthedocs.io/en/latest/types/item_action_types 
[4]: ../block_action_types.md 
[5]: ../item_condition_types.md 
[6]: ../block_condition_types.md 
[7]: https://origins.readthedocs.io/en/latest/types/data_types/array
[8]: https://origins.readthedocs.io/en/latest/types/data_types/string 
[9]: https://origins.readthedocs.io/en/latest/types/data_types/item_stack
