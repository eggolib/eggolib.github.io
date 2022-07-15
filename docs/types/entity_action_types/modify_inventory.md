---
title: Modify Inventory (Entity Action Types)
date: 2022-07-14
---

#   Modify Inventory

**[Entity Action Type]**

Modifies the item(s) from either the entity's inventory or a power that uses the **[Inventory (Power Type)]** (or **[Origins/Apoli's Inventory (Power Type)]**).

Type ID: `eggolib:modify_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | **[Inventory Type]** | `"inventory"` | Determines whether to modify the items in the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the entity **before** the items are modified.
`item_action` | **[Item Action Type]** | | The action to execute on the affected items.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only items which fulfill this condition will be affected by the specified action.
`slot` | **[Identifier]** | *optional* | If specified, only items in the designated slot will be modified. See **[Positioned Item Stack Slots]** for possible values.
`slots` | **[Array]** of **[Identifiers]** | *optional* | If specified, only items in the designated slots will be modified. See **[Positioned Item Stack Slots]** for possible values.
`power` | **[Identifier]** | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be modified instead of the items in the entity's inventory.


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



[Inventory (Power Type)]: ../power_types/inventory.md
[Origins/Apoli's Inventory (Power Type)]: https://origins.readthedocs.io/en/latest/types/power_types/inventory/
[Entity Action Type]: ../entity_action_types.md
[Inventory Type]: https://origins.readthedocs.io/en/latest/misc/extras/inventory_type
[Item Action Type]: https://origins.readthedocs.io/en/latest/types/item_action_types
[Item Condition Type]: ../item_condition_types.md
[Identifier]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[Identifiers]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Positioned Item Stack Slots]: https://origins.readthedocs.io/en/latest/misc/extras/positioned_item_stack_slots
[Item Stack]: https://origins.readthedocs.io/en/latest/types/data_types/item_stack
