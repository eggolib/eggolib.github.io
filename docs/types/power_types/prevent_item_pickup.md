---
title: Prevent Item Pickup (Power Types)
date: 2022-08-24
search:
    boost: 2
---

#   Prevent Item Pickup

**[Power Type]**

Prevents the entity that has the power from picking up an item.

Type ID: `eggolib:prevent_item_pickup`

!!! note

    In the context of this power type, the '**actor**' entity is the entity that may have thrown the item while the '**target**' entity is the entity that has attempted to pick up an item.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | **[Bi-entity Action Type]** | *optional* | If specified, this action will be executed on either or both the '**actor**' and '**target**' entities upon the '**target**' entity being prevented from picking up an item.
`item_action` | **[Item Action Type]** | *optional* | If specified, this action will be executed on the item that was attempted to be picked up.
`bientity_condition` | **[Bi-entity Condition Type]** | *optional* | If specified, only prevent the item from being picked up and execute the actions if this condition is fulfilled by either or both the '**actor**' and '**target**' entities.
`item_condition` | **[Item Condition Type]** | *optional* | If specified, only items that fulfills this condition will be prevented from being picked up.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:prevent_item_pickup",
        "item_condition": {
            "type": "eggolib:block_item"
        }
    }
    ```

    This example will prevent the entity that has the power from picking up any block items.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:prevent_item_pickup",
        "bientity_condition": {
            "type": "eggolib:has_matching_tag",
            "inverted": true
        },
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:diamond"
            }
        }
    }
    ```

    This example will prevent the entity that has the power from picking up a Diamond item if that said item is thrown by an entity that doesn't have a matching tag with the entity that has the power.



[Power Type]: ../power_types.md
[Bi-entity Action Type]: ../bientity_action_types.md
[Item Action Type]: https://origins.readthedocs.io/en/latest/types/item_action_types
[Bi-entity Condition Type]: ../bientity_condition_types.md
[Item Condition Type]: ../item_condition_types.md
