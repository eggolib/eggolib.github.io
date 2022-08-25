---
title: Drop Inventory (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Drop Inventory

**[Entity Action Type]**

Drops the item(s) from either the entity's inventory or a power that uses the **[Inventory (Power Type)]** or **[Origins/Apoli's Inventory (Power Type)]**.

Type ID: `eggolib:drop_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | **[Inventory Type]** | `"inventory"` | Determines whether to drop the items from the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the entity **before** the items are dropped.
`item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the affected items **before** the said items are dropped
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only items which fulfill this condition will be dropped.
`slot` | **[Identifier]** | *optional* | If specified, only items in the designated slot will be dropped. See **[Positioned Item Stack Slots]** for possible values.
`slots` | **[Array]** of **[Identifiers]** | *optional* | If specified, only items in the designated slots will be dropped. See **[Positioned Item Stack Slots]** for possible values.
`power` | **[Identifier]** | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be dropped instead of the items in the entity's inventory.
`amount` | **[Integer]** | *optional* | If specified, the affected items will be split by this amount.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:drop_inventory"
    }
    ```

    This example will drop the entire inventory of the entity.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:drop_inventory",
        "item_condition": {
            "type": "apoli:amount",
            "comparison": ">=",
            "compare_to": 10
        }
    }
    ```

    This example will drop items from the inventory of the entity only if those items have an amount of 10 or greater.


=== "Example #3"

    ``` json
    "entity_action": {
        "type": "eggolib:drop_inventory",
        "slot": "weapon.mainhand",
        "amount": 16
    }
    ```

    This example will split the item from the entity's mainhand slot by 16 and drop it. For a further explanation, if the item from the entity's mainhand slot has a count of 64, only 16 of it will be dropped, making the item have a remainder of 48. *(64 - 16 = 48)*



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
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer
