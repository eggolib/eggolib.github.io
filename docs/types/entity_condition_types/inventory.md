---
title: Inventory (Entity Condition Type)
date: 2022-07-29
search:
    boost: 2
---

#   Inventory

**[Entity Condition Type]**

Checks if the inventory of the entity is occupied.

Type ID: `eggolib:inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | **[Inventory Type]** | `"inventory"` | Determines whether to check for items in the inventory of the entity or the inventory of a power present in the entity.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only evaluate the condition to true if any of the items in the specified inventory fulfills this condition.
`slot` | **[Identifier]** | *optional* | If specified, only items in the specified slot will be checked. See **[Positioned Item Stack Slots]** for possible values.
`slots` | **[Array]** of **[Identifiers]** | *optional* | If specified, only items in the specified slots will be checked. See **[Positioned Item Stack Slots]** for possible values.
`power` | **[Identifier]** | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be checked instead of the items in the entity's inventory.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:inventory",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:egg"
            }
        }
    }
    ```

    This example will check if the entity has an Egg item in their inventory.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:inventory",
        "inventory_type": "power",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:nether_star"
            }
        },
        "slot": "container.4",
        "power": "origins:shulker_inventory"
    }
    ```

    This example will check if the entity has a Nether Star in the middle slot of the inventory of the `origins:shulker_inventory` power.



[Entity Condition Type]: ../entity_condition_types.md
[Inventory Type]: https://origins.readthedocs.io/en/latest/misc/extras/inventory_type
[Item Condition Type]: ../item_condition_types.md
[Identifier]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[Positioned Item Stack Slots]: https://origins.readthedocs.io/en/latest/misc/extras/positioned_item_stack_slots
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Identifiers]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
