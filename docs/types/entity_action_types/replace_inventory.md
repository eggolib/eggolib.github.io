---
title: Replace Inventory (Entity Action Types)
date: 2022-07-14
---

#   Replace Inventory

**[Entity Action Type]**

Replaces the item(s) from either the entity's inventory or a power that uses the **[Inventory (Power Type)]** or **[Origins/Apoli's Inventory (Power Type)]**.

Type ID: `eggolib:replace_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`inventory_type` | **[Inventory Type]** | `"inventory"` | Determines whether to replace the items from the inventory of the entity or the inventory of a power present in the entity.
`entity_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the entity **before** the items are replaced.
`item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the affected items **after** the said items are replaced.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only items which fulfill this condition will be replaced.
`slot` | **[Identifier]** | *optional* | If specified, only items in the designated slot will be replaced. See **[Positioned Item Stack Slots]** for possible values.
`slots` | **[Array]** of **[Identifiers]** | *optional* | If specified, only items in the designated slots will be replaced. See **[Positioned Item Stack Slots]** for possible values.
`power` | **[Identifier]** | *optional* | If specified and if `inventory_type` is set to `"power"`, the items in the inventory of this power will be replaced instead of the items in the entity's inventory.
`stack` | **[Item Stack]** | | The item to use as a replacement for the affected items.
`merge_nbt` | **[Boolean]** | `false` | Determines whether to merge the NBTs of the item that will be replaced and the NBTs of the item that will be used as a replacement.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:replace_inventory",
        "stack": {
            "item": "minecraft:egg"
        }
    }
    ```

    This example will fill the entire inventory of the entity with Eggs.

=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:replace_inventory",
        "slots": [
            "weapon.mainhand",
            "weapon.offhand"
        ],
        "stack": {
            "item": "minecraft:air"
        }
    }
    ```

    This example will remove the items from the entity's off and main hands.


=== "Example #3"

    ``` json
    "entity_action": {
        "type": "eggolib:replace_inventory",
        "slot": "weapon.mainhand",
        "stack": {
            "item": "minecraft:wooden_sword",
            "tag": "{Enchantments: [{id: \"minecraft:mending\", lvl: 1s}]}"
        },
        "merge_nbt": true
    }
    ```

    This example will replace the item from the entity's mainhand slot with a Wooden Sword enchanted with the Mending enchantment. If the previous item from the entity's mainhand slot had NBTs, those NBTs will be merged to the NBTs of the item used as a replacement.



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
[Boolean]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
