---
title: Generalized Positioned Item Stack (Data Type)
date: 2022-10-15
search:
    boost: 2
---

#   Generalized Positioned Item Stack

[**Data Type**][1]

An [**object**][2] that defines an item stack alongside a position in an inventory; generalized to all entities that may have a stack reference.


!!! note

    Refer to [**Minecraft Fandom: Slot (Command argument)**][3] for the string values you can use in the `slot` field of this data type.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`item` | [**Identifier**][4] | | The namespace and ID of the item.
`amount` | [**Integer**][5] | `1` | The size of the item.
`tag` | [**String**][6] | *optional* | The NBT data of the item.
`slot` | [**String**][6] | *optional* | The position for the item in the inventory of an entity.


### Examples

=== "Example #1"

    ``` json
    "stack": {
        "item": "minecraft:diamond",
        "amount": 16
    }
    ```

    This example will define a new Diamond item stack with a size of 16.


=== "Example #2"

    ``` json
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
    ```

    This example will define two new item stacks: a Shield that will be placed in the offhand equipment slot of the entity and an Iron Sword that will be placed in the mainhand equipment slot of the entity.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/object
[3]: https://minecraft.fandom.com/wiki/Slot#Command_argument
[4]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[5]: https://origins.readthedocs.io/en/latest/types/data_types/integer
[6]: https://origins.readthedocs.io/en/latest/types/data_types/string
