---
title: Modify Inventory (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Modify Inventory

[**Entity Action Type**][1]

Modifies the item(s) from either the entity's inventory or a power that uses the [**Inventory (Power Type)**][2] or [**Origins/Apoli's Inventory (Power Type)**][3].

Type ID: `eggolib:modify_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | [**Inventory Type**][4] | `"inventory"` | Determines whether to modify the items in the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | [**Entity Action**][5] | *optional* | If specified, this action will be executed on the entity **before** the items are modified.
`item_action` | [**Item Action**][6] | | The action to execute on the affected items.
`item_condition` | [**Item Condition**][7] | *optional* | If specified, only items which fulfill this condition will be affected by the specified action.
`slot` | [**Identifier**][8] | *optional* | If specified, only items in the designated slot will be modified. See [**Positioned Item Stack Slots**][9] for possible values.
`slots` | [**Array**][10] of [**Identifiers**][8] | *optional* | If specified, only items in the designated slots will be modified. See [**Positioned Item Stack Slots**][9] for possible values.
`power` | [**Identifier**][8] | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be modified instead of the items in the entity's inventory.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_inventory",
        "item_action": {
            "type": "apoli:consume",
            "amount": 1
        }
    }
    ```

    This example will "consume" all items from the entity's inventory.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_inventory",
        "item_action": {
            "type": "apoli:damage",
            "amount": 5
        },
        "item_condition": {
            "type": "apoli:armor_value",
            "comparison": ">",
            "compare_to": 0
        },
        "slots": [
            "armor.head",
            "armor.chest",
            "armor.legs",
            "armor.feet"
        ]
    }
    ```

    This example will damage armor items from the entity's equipment armor slots.



[1]: ../entity_action_types.md
[2]: ../power_types/inventory.md
[3]: https://origins.readthedocs.io/en/latest/types/power_types/inventory
[4]: https://origins.readthedocs.io/en/latest/misc/extras/inventory_type
[5]: ../entity_action_types.md
[6]: https://origins.readthedocs.io/en/latest/types/item_action_types
[7]: ../item_condition_types.md
[8]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[9]: https://origins.readthedocs.io/en/latest/misc/extras/positioned_item_stack_slots
[10]: https://origins.readthedocs.io/en/latest/types/data_types/array
