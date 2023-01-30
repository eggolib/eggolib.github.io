---
title: Modify Breathing (Power Type)
date: 2023-01-30
search:
    boost: 2
---

#   Modify Breathing

[**Power Type**][1]

Modifies how the entity that has the power breathes.

Type ID: `eggolib:modify_breathing`


!!! note

    The base values for gaining and losing air is 4 and 1 respectively.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`breathable_block_condition` | [**Block Condition Type**][2] | | Determines which block the entity will be able to breathe in.
`breathing_status_effect` | [**Identifier**][3] | *optional* | If specified, the entity will be able to maintain their breath if they have this status effect.
`breathing_status_effects` | [**Array**][4] of [**Identifiers**][3] | *optional* | If specified, the entity will be able to maintain their breath if they have one of these status effects.
`gain_air_modifier` | [**Attribute Modifier**][5] | *optional* | If specified, this modifier will be applied to the air gained by breathing in a breathable block.
`gain_air_modifiers` | [**Array**][4] of [**Attribute Modifiers**][5] | *optional* | If specified, these modifiers will be applied to the air gained by breathing in a breathable block.
`gain_air_interval` | [**Positive Integer**][6] | `1` | Determines how frequent should the entity gain air.
`lose_air_modifier` | [**Attribute Modifier**][5] | *optional* | If specified, this modifier will be applied to the air lost by not breathing in a breathable block.
`lose_air_modifiers` | [**Array**][4] of [**Attribute Modifiers**][5] | *optional* | If specified, these modifiers will be applied to the air lost by not breathing in a breathable block.
`lose_air_interval` | [**Positive Integer**][6] | `1` | Determines how frequent should the entity lose air.
`damage_source` | [**Damage Source**][7] | *optional* | If specified, this damage source will be used instead when dealing damage to the entity upon not being able to breathe.
`damage_modifier` | [**Attribute Modifier**][5] | *optional* | If specified, this modifier will be applied to the damage dealt to the entity upon not being able to breathe.
`damage_modifiers` | [**Array**][4] of [**Attribute Modifiers**][5] | *optional* | If specified, these modifiers will be applied to the damage dealt to the entity upon not being able to breathe.
`damage_interval` | [**Positive Integer**][6] | `20` | Determines how frequent the damage should be dealt to the entity upon not being able to breathe.
`particle` | [**Particle Effect**][8] | *optional* | If specified, this particle will be emitted instead upon being damaged for not being able to breathe.
`ignore_respiration` | [**Boolean**][9] | `false` | Determines whether the power should ignore the effects of the Respiration enchantment.
`priority` | [**Integer**][10] | `0` | Determines the priority of the power. The power with the highest priority value will be used.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_breathing",
        "breathable_block_condition": {
            "type": "apoli:fluid",
            "fluid_condition": {
                "type": "apoli:in_tag",
                "tag": "minecraft:lava"
            }
        }
    }
    ```

    This example will make the entity only be able to breathe in Lava.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:modify_breathing",
        "breathable_block_condition": {
            "type": "apoli:fluid",
            "fluid_condition": {
                "type": "apoli:in_tag",
                "tag": "minecraft:water"
            }
        },
        "breathing_status_effect": "minecraft:water_breathing",
        "lose_air_modifier": {
            "operation": "addition",
            "value": 3
        }
    }
    ```

    This example will make the entity only be able to breathe in Water unless they have the Water Breathing status effect, which they can use to breathe on land.



[1]: ../power_types.md
[2]: ../block_condition_types.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[4]: https://origins.readthedocs.io/en/latest/types/data_types/array
[5]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[6]: ../data_types/positive_integer.md
[7]: https://origins.readthedocs.io/en/latest/types/data_types/damage_source
[8]: https://origins.readthedocs.io/en/latest/types/data_types/particle_effect
[9]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
[10]: https://origins.readthedocs.io/en/latest/types/data_types/integer
