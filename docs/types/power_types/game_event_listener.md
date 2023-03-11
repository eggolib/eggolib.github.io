---
title: Game Event Listener (Power Type)
date: 2023-01-30
search:
    boost: 2
---

#   Game Event Listener

[**Power Type**][1]

Executes an action upon listening to certain game events or vibrations.

Type ID: `eggolib:game_event_listener`


!!! note

    See [**Minecraft Fandom: Sculk Sensor (Vibration amplitudes)**][2] for a list of vanilla game events you can use.


!!! note

    In the context of this power, the 'actor' will be the entity that emitted the game event whilst the 'target' will be the entity that has the power.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_action` | [**Block Action Type**][3] | *optional* | If specified, this action will be executed at the position where the game event was emitted.
`bientity_action` | [**Bi-Entity Condition Type**][4] | *optional* | If specified, this action will be executed on either or both the 'actor' and the 'target' upon listening to certain game event(s).
`block_condition` | [**Block Condition Type**][5] | *optional* | If specified, the power will only listen to the game event if the block that emitted it fulfills this condition.
`bientity_condition` | [**Bi-Entity Condition Type**][4] | *optional* | If specified, the power will only listen to the game event if either or both the 'actor' that emitted it and the 'target' fulfill this condition.
`cooldown` | [**Positive Integer**][6] | `1` | Interval of ticks the power needes to recharge before the power can be triggered again.
`hud_render` | [**HUD Render**][7] | *optional* | If specified, determines how the cooldown of the power is visualized in the HUD.
`range` | [**Positive Integer**][6] | `16` | Determines how far the power can listen for game events.
`event` | [**Identifier**][8] | *optional* | If specified, the power will only listen to this game event.
`events` | [**Array**][9] of [**Identifiers**][8] | *optional* | If specified, the power will only listen to these game events.
`tag` | [**Identifier**][8] | *optional* | If specified, the power will only listen to the game events included in this game event tag.
`show_particle` | [**Boolean**][10] | `true` | Determines whether the vibration particle is spawned when a game event is accepted.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:game_event_listener",
        "block_action": {
            "type": "apoli:set_block",
            "block": "minecraft:stone"
        },
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:bell"
        },
        "range": 32
    }
    ```

    This example will replace Bells that emits a vibration within a 32 blocks radius with Stone.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:game_event_listener",
        "bientity_action": {
            "type": "apoli:invert",
            "action": {
                "type": "eggolib:damage",
                "source": {
                    "name": "player"
                },
                "modifier": {
                    "operation": "multiply_total_multiplicative",
                    "value": 0.25
                }
            }
        },
        "bientity_condition": {
            "type": "apoli:actor_condition",
            "condition": {
                "type": "apoli:entity_type",
                "entity_type": "minecraft:creeper"
            }
        },
        "event": "minecraft:step"
    }
    ```

    This example will damage Creepers emitting a `minecraft:step` vibration *(via walking)* within a 16 blocks radius.


=== "Example #3"

    ```json
    {
        "type": "eggolib:game_event_listener",
        "bientity_action": {
            "type": "apoli:apply_effect",
            "effect": {
                "effect": "minecraft:darkness",
                "amplifier": 1,
                "duration": 100
            }
        },
        "bientity_condition": {
            "type": "apoli:and",
            "conditions": [
                {
                    "type": "apoli:target_condition",
                    "condition": {
                        "type": "apoli:exists"
                    }
                },
                {
                    "type": "eggolib:equal",
                    "inverted": true
                }
            ]
        },
        "show_particle": false
    }
    ```

    This example will apply the Darkness II (00:05) status effect to entities *(except the entity that has the power)* within a 16 blocks radius without showing the Vibration particle.



[1]: ../power_types.md
[2]: https://minecraft.fandom.com/wiki/Sculk_Sensor#Vibration_amplitudes
[3]: ../block_action_types.md
[4]: ../bientity_condition_types.md
[5]: ../block_condition_types.md
[6]: ../data_types/positive_integer.md
[7]: https://origins.readthedocs.io/en/latest/types/data_types/hud_render
[8]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[9]: https://origins.readthedocs.io/en/latest/types/data_types/array
[10]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
