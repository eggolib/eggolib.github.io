---
title: Inventory (Entity Condition Type)
date: 2022-07-29
search:
    boost: 2
---

#   Inventory

[**Entity Condition Type**][1]

Checks if the inventory of the entity is occupied.

Type ID: `eggolib:inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | [**Inventory Type**][2] | `"inventory"` | Determines whether to check for items in the inventory of the entity or the inventory of a power present in the entity.
`item_condition` | [**Item Condition**][3] | *optional* | If specified, only evaluate the condition to true if any of the items in the specified inventory fulfills this condition.
`comparison` | [**Comparison**][4] | `">"` | Determines the amount of items that were found is compared to the specified value.
`compare_to` | [**Integer**][5] | `0` | The value which the amount of items that were found is compared to.
`slot` | [**Identifier**][6] | *optional* | If specified, only items in the specified slot will be checked. See [**Positioned Item Stack Slots**][7] for possible values.
`slots` | [**Array**][8] of [**Identifiers**][6] | *optional* | If specified, only items in the specified slots will be checked. See [**Positioned Item Stack Slots**][7] for possible values.
`power` | [**Identifier**][6] | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be checked instead of the items in the entity's inventory.


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



[1]: ../entity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/misc/extras/inventory_type
[3]: ../item_condition_types.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[5]: https://origins.readthedocs.io/en/latest/types/data_types/integer
[6]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[7]: https://origins.readthedocs.io/en/latest/misc/extras/positioned_item_stack_slots
[8]: https://origins.readthedocs.io/en/latest/types/data_types/array
