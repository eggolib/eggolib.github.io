---
title: Fire Projectile (Entity Action Type)
date: 2023-01-30
search:
    boost: 2
---

#   Fire Projectile

[**Entity Action Type**][1]

Fires one or more projectiles or entities.

Type ID: `eggolib:fire_projectile`


!!! note

    This action type can spawn in entities with passengers.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_type` | [**Identifier**][2] | | The identifier of the projectile or entity that will be launched.
`divergence` | [**Float**][3] | `1.0` | Determines how much the projectile or entity that will be launched is affected by random spread.
`speed` | [**Float**][3] | `1.0` | Determines the speed of the projectile or entity that will be launched.
`count` | [**Integer**][4] | `1` | Determines the amount of projectiles or entities that will be launched.
`tag` | [**String**][5] | *optional* | If specified, this NBT data will be added to the projectile or entity that will be launched.
`entity_action` | [**Entity Action Type**][1] | *optional* | If specified, this action will be executed on the projectile or entity that will be launched.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:fire_projectile",
        "entity_type": "minecraft:fireball"
    }
    ```

    This example will launch a Fireball in the direction the entity is facing.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:fire_projectile",
        "entity_type": "minecraft:pig",
        "tag": "{Passengers: [{id: \"minecraft:armor_stand\"}]}"
    }
    ```

    This example will launch a Pig with an Armor Stand passenger.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/float
[4]: https://origins.readthedocs.io/en/latest/types/data_types/integer
[5]: https://origins.readthedocs.io/en/latest/types/data_types/string
