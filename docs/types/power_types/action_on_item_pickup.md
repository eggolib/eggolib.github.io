---
title: Action on Item Pickup (Power Type)
date: 2022-08-24
search:
    boost: 2
---

#   Action on Item Pickup

[**Power Type**][1]

Executes an action upon picking up an item.

Type ID: `eggolib:action_on_item_pickup`


!!! note

    In the context of this power type, the '**actor**' entity is the entity that may have thrown the item while the '**target**' entity is the entity that picked up the item.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [**Bi-entity Action Type**][2] | *optional* | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities.
`item_action` | [**Item Action Type**][3] | *optional* | If specified, this action will be executed on the item that was picked up.
`bientity_condition` | [**Bi-entity Condition Type**][4] | *optional* | If specified, the actions will only be executed if this condition is fulfilled by either or both the '**actor**' and '**target**' entities.
`item_condition` | [**Item Condition Type**][5] | *optional* | If specified, the actions will only be executed if this condition is fulfilled by the item about to be picked up.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:action_on_item_pickup",
        "bientity_action": {
            "type": "apoli:execute_command",
            "command": "me has picked up an item!"
        }
    }
    ```

    This example will notify all players that the entity that has the power has picked up an item.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:action_on_item_pickup",
        "item_action": {
            "type": "apoli:merge_nbt",
            "nbt": "{Enchantments: [{id: \"minecraft:vanishing_curse\", lvl: 1s}]}"
        },
        "item_condition": {
            "type": "eggolib:tool",
            "tool_types": [
                "pickaxe",
                "axe",
                "shovel",
                "hoe"
            ]
        }
    }
    ```

    This example will enchant the pickaxe, axe, shovel and hoe tool items with Curse of Vanishing I upon being picked up by the entity that has the power.


=== "Example #3"

    ``` json
    {
        "type": "eggolib:action_on_item_pickup",
        "bientity_action": {
            "type": "apoli:target_action",
            "action": {
                "type": "apoli:execute_command",
                "command": "me has picked up someone else's item!"
            }
        },
        "bientity_condition": {
            "type": "apoli:actor_condition",
            "condition": {
                "type": "apoli:exists"
            }
        }
    }
    ```

    This example will notify all players that the entity that has the power has picked up an item thrown by another entity.



[1]: ../power_types.md
[2]: ../bientity_action_types.md 
[3]: https://origins.readthedocs.io/en/latest/types/item_action_types 
[4]: ../bientity_condition_types.md 
[5]: ../item_condition_types.md
