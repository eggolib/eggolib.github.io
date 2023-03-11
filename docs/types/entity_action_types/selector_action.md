---
title: Selector Action (Entity Action Type)
date: 2023-03-11
search:
    boost: 2
---

#   Selector Action

[**Entity Action Type**][1]

Executes an action on entities selected by a target selector.

Type ID: `eggolib:selector_action`


!!! note

    See [**Minecraft Fandom Wiki: Target selectors**][2] for more information about target selectors.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`selector` | [**String**][3] | | The selector to use for selecting entities. It can be the username of a player, the UUID of the entity or a target selector.
`bientity_action` | [**Bi-entity Action Type**][4] | *optional* | If specified, this action will be executed on either or both the actor and target entities.
`bientity_condition` | [**Bi-entity Condition Type**][5] | *optional* | If specified, the specified action will only be executed if this condition is fulfilled by either or both the actor and target entities.


### Examples

=== "Example #1"

    ```json
    "entity_action": {
        "type": "eggolib:selector_action",
        "selector": "Steve",
        "bientity_action": {
            "type": "apoli:damage",
            "amount": 5,
            "source": {
                "name": "generic"
            }
        }
    }
    ```

    This example will deal 2 and a half hearts of damage to the player named Steve.


=== "Example #2"

    ```json
    "entity_action": {
        "type": "eggolib:selector_action",
        "selector": "@e[type = minecraft:armor_stand, tag = some_tag]",
        "bientity_action": {
            "type": "apoli:target_action",
            "action": {
                "type": "apoli:execute_command",
                "command": "kill @s"
            }
        }
    }
    ```

    This example will kill Armor Stands that have the `some_tag` tag *(added via the `/tag` command)*



[1]: ../entity_action_types.md
[2]: https://minecraft.fandom.com/wiki/Target_selectors
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
[4]: ../bientity_action_types
[5]: ../bientity_condition_types.md
