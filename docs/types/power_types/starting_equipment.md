---
title: Starting Equipment (Power Type)
date: 2022-10-15
search:
    boost: 2
---

#   Starting Equipment

[**Power Type**][1]

Provides the entity with the specified items when the power is granted.

Type ID: `eggolib:starting_equipment`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`stack` | [**Generalized Positioned Item Stack**][2] | *optional* | If specified, this item stack will be given to the entity.
`stacks` | [**Array**][3] of [**Generalized Positioned Item Stack**][2] | *optional* | If specified, these item stacks will be given to the entity.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:starting_equipment",
        "stack": {
            "item": "minecraft:glass",
            "slot": "armor.head"
        }
    }
    ```

    This example will provide a Glass block on the entity's head.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:starting_equipment",
        "stacks": [
            {
                "item": "minecraft:shield",
                "slot": "weapon.offhand"
            },
            {
                "item": "minecraft:iron_sword",
                "slot": "weapon.mainhand"
            }
        ]
    }
    ```

    This example will provide a Shield and an Iron Sword to the entity in its offhand and mainhand equipment slots respectively.



[1]: ../power_types.md
[2]: ../data_types/generalized_positioned_item_stack.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
