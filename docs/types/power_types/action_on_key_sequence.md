---
title: Action on Key Sequence (Power Types)
date: 2022-08-24
search:
    boost: 2
---

#   Action on Key Sequence

**[Power Type]**

Executes an action upon pressing certain keybinds in a certain sequence.

Type ID: `eggolib:action_on_key_sequence`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`success_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed if the player succeeded to press the specified keybinds in the specified sequence.
`fail_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed if the player failed to press the specified keybinds in the specified sequence.
`cooldown` | **[Integer]** | `0` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | **[HUD Render]** | `{"should_render": false}` | Determines how the cooldown for this power is visualized on the HUD.
`keys` | **[Array ]**of **[Functional Keys]** | | Determines the keys to be used for completing the sequence.
`key_sequence` | **[Array]** of **[Keys]** | | Determines the sequence to be completed by the player.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:action_on_key_sequence",
        "success_action": {
            "type": "apoli:heal",
            "amount": 4
        },
        "cooldown": 100,
        "hud_render": {
            "should_render": true
        },
        "keys": [
            {
                "key": "key.jump",
                "continuous": false,
                "action": {
                    "type": "apoli:execute_command",
                    "command": "me jumped!"
                }
            },
            "key.attack",
            "key.use"
        ],
        "key_sequence": [
            "key.attack",
            "key.attack",
            "key.jump"
        ]
    }
    ```

    This example will heal the player with 4 health points *(or 2 hearts)* upon the player pressing the `key.attack` and `key.jump` keybinds in a `key.attack` -> `key.attack` -> `key.jump` sequence.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:action_on_key_sequence",
        "success_action": {
            "type": "apoli:execute_command",
            "command": "me casted 'KONAMI CODE'!"
        },
        "fail_action": {
            "type": "apoli:damage",
            "source": {
                "name": "generic"
            },
            "amount": 10
        },
        "cooldown": 200,
        "hud_render": {
            "should_render": true
        },
        "keys": [
            {
                "key": "key.jump",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say UP"
                }
            },
            {
                "key": "key.sneak",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say DOWN"
                }
            },
            {
                "key": "key.left",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say LEFT"
                }
            },
            {
                "key": "key.right",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say RIGHT"
                }
            },
            {
                "key": "key.attack",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say A (Attack)"
                }
            },
            {
                "key": "key.use",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "say B (Use)"
                }
            }
        ],
        "key_sequence": [
            "key.jump",
            "key.jump",
            "key.sneak",
            "key.sneak",
            "key.left",
            "key.right",
            "key.left",
            "key.right",
            "key.use",
            "key.attack"
        ]
    }
    ```

    This example will notify all players that the player that has the power has *"casted 'KONAMI CODE'!"* if the player in question has pressed the `key.jump`, `key.sneak`, `key.left`, `key.right`, `key.attack` and `key.use` keybinds in the classic KONAMI CODE sequence.
    *(UP (`key.jump`) -> UP (`key.jump`) -> DOWN (`key.sneak`) -> DOWN (`key.sneak`) -> LEFT (`key.left`) -> RIGHT (`key.right`) -> LEFT (`key.left`) -> RIGHT (`key.right`) -> B (`key.use`) -> A (`key.attack`))*



[Power Type]: ../power_types.md
[Entity Action Type]: ../entity_action_types.md
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer
[HUD Render]: https://origins.readthedocs.io/en/latest/types/data_types/hud_render
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Functional Keys]: ../data_types/functional_key.md
[Keys]: ../data_types/key.md
