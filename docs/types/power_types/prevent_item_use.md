---
title: Prevent Item Use (Power Type)
date: 2022-07-27
search:
    boost: 1
---

#   Prevent Item Use

**[Power Type]**

Prevents the player from "using" *(e.g: right-click action, such as eating, blocking, etc.)* items.

Type ID: `eggolib:prevent_item_use`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the player that has the power upon being prevented from using an item.
`held_item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the item that was prevented from being used.
`result_item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the item that is given upon being prevented from using an item.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only items that fulfills this condition will be prevented from being used.
`result_stack` | **[Item Stack]** | *optional* | If specified, this item will be given to the player upon being prevented from using an item.
`hands` | **[Array]** of **[Strings]** | `["main_hand", "off_hand"]` | Determines if the power should prevent the usage of items from the specified hand(s). Accepts `"main_hand"`, `"off_hand"` or both.
`priority` | **[Integer]** | 0 | Determines the execution priority of the power.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:prevent_item_use",
        "hands": [
            "off_hand"
        ]
    }
    ```

    This example will prevent the player from using items in the offhand slot.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:prevent_item_use",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:shield"
            }
        },
        "hands": [
            "main_hand"
        ]
    }
    ```

    This example will prevent the player from using Shields in the mainhand slot.



[Power Type]: ../power_types.md
[Entity Action Type]: ../entity_action_types.md
[Item Action Type]: https://origins.readthedocs.io/en/latest/types/item_action_types
[Item Condition Type]: ../item_condition_types.md
[Item Stack]: https://origins.readthedocs.io/en/latest/types/data_types/item_stack
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Strings]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer