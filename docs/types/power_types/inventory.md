---
title: Inventory (Power Type)
date: 2022-07-14
search:
    boost: 2
---

#   Inventory

[**Power Type**][1]

Provides an inventory that can be opened with the specified key, which may or may not persist on death.

Type ID: `eggolib:inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`title` | [**String**][2] | `"container.inventory"` | The translation key or literal text to use as the display name for the inventory.
`container_type` | [**Container Type**][3] | `"dropper"` | Determines what type of container preset the inventory will use.
`drop_on_death` | [**Boolean**][4] | `false` | If set to true, the player will drop the items from the inventory on death. Items with the Curse of Vanishing enchantment will also vanish.
`drop_on_death_filter` | [**Item Condition Type**][5] | *optional* | If specified, only the item stack(s) that fulfill this condition will be dropped on death.
`recoverable` | [**Boolean**][4] | `true` | Determines if the contents of the inventory should be dropped upon losing the power.
`key` | [**Key**][6] | *optional* | The keybind this power is bound to.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:inventory",
        "container_type": "chest",
        "key": {
            "key": "key.hotbar.9"
        }
    }
    ```

    This example will provide an inventory with a size similar to a single Chest that can be opened with the `key.hotbar.9` keybind.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:inventory",
        "title": "Pockets",
        "container_type": "hopper",
        "key": {
            "key": "key.use"
        },
        "condition": {
            "type": "apoli:and",
            "conditions": [
                {
                    "type": "apoli:equipped_item",
                    "equipment_slot": "mainhand",
                    "item_condition": {
                        "type": "apoli:empty"
                    }
                },
                {
                    "type": "apoli:equipped_item",
                    "equipment_slot": "offhand",
                    "item_condition": {
                        "type": "apoli:empty"
                    }
                }
            ]
        }
    }
    ```

    This example will provide an inventory with a size similar to a Hopper that can be opened using the `key.use` keybind while holding no items in the mainhand and the offhand.



[1]: ../power_types.md
[2]: https://origins.readthedocs.io/en/latest/types/string 
[3]: https://origins.readthedocs.io/en/latest/misc/extras/container_type 
[4]: https://origins.readthedocs.io/en/latest/types/data_types/boolean 
[5]: ../item_condition_types.md 
[6]: https://origins.readthedocs.io/en/latest/types/data_types/key
