---
title: Stat (Power Type)
date: 2023-06-18
search:
    boost: 2
---

#   Stat

[**Power Type**][1]

Tracks the effective value of the specified statistic; essentially works the same as the [**Resource (Power Type)**][2].

Type ID: `eggolib:stat`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`stat` | [**Stat**][3] | | The statistic to keep track the value of.
`on_change_action` | [**Entity Action Type**][4] | *optional* | If specified, this action will be executed on the entity if the stored value is changed.
`min_action` | [**Entity Action Type**][4] | *optional* | If specified, this action will be executed once the minimum value is reached.
`max_action` | [**Entity Action Type**][4] | *optional* | If specified, this action will be executed once the maximum value is reached.
`hud_render` | [**HUD Render**][5] | *optional* | Determines how the stored value is visualized in the HUD.
`min` | [**Integer**][6] | `0` | The minimum value that is allowed to be stored in the power
`max` | [**Integer**][6] | `2147483647` | The maximum value that is allowed to be stored in the power.
`start_value` | [**Integer**][6] | The value of the `min` field | The stored starting value upon gaining the power.


### Examples

=== "Example #1"

    ```json
    {
        "type": "eggolib:stat",
        "stat": {
            "type": "custom",
            "id": "minecraft:damage_dealt"
        },
        "max": 100,
        "hud_render": {
            "should_render": true
        }
    }
    ```

    This example will keep track of the effective value of the `minecraft.custom:minecraft.damage_dealt` statistic of the player, with a maximum value of 100.


=== "Example #2"

    ```json
    {
        "type": "eggolib:stat",
        "stat": {
            "type": "mined",
            "id": "minecraft:sand"
        }
    }
    ```

    This example will keep track of the effective value of the `minecraft.mined:minecraft.sand` statistic of the player.



[1]: ../power_types.md
[2]: https://origins.readthedocs.io/en/latest/types/power_types/resource
[3]: https://origins.readthedocs.io/en/latest/types/data_types/stat
[4]: ../entity_action_types.md
[5]: https://origins.readthedocs.io/en/latest/types/data_types/hud_render
[6]: https://origins.readthedocs.io/en/latest/types/data_types/integer
