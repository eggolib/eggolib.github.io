---
title: Action on Key Sequence (Power Type)
date: 2022-08-24
search:
    boost: 2
---

#   Action on Key Sequence

[**Power Type**][1]

Executes an action upon pressing certain keybinds in a certain sequence.

Type ID: `eggolib:action_on_key_sequence`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`success_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed if the player succeeded to press the specified keybinds in the specified sequence.
`fail_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed if the player failed to press the specified keybinds in the specified sequence.
`cooldown` | [**Integer**][3] | `0` | Interval of ticks this power needs to recharge before the power can be triggered again.
`hud_render` | [**HUD Render**][4] | `{"should_render": false}` | Determines how the cooldown for this power is visualized on the HUD.
`keys` | [**Array**][5] of [**Functional Keys**][6] | | Determines the keys to be used for completing the sequence.
`key_sequence` | [**Array**][5] of [**Keys**][7] | | Determines the sequence to be completed by the player.


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



[1]: ../power_types.md
[2]: ../entity_action_types.md 
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer 
[4]: https://origins.readthedocs.io/en/latest/types/data_types/hud_render 
[5]: https://origins.readthedocs.io/en/latest/types/data_types/array 
[6]: ../data_types/functional_key.md 
[7]: ../data_types/key.md
