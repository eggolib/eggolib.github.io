---
title: Modify (Item Action Type)
date: 2023-06-18
search:
    boost: 2
---

#   Modify

[**Item Action Type**][1]

Applies an item modifier to the item stack.

Type ID: `eggolib:modify`


!!! note

    This item action type has the following loot context:

    * The origin position of the item modifier; X: 0, Y: 0 and Z: 0 by default.
    * `this` entity; the holder of the item stack.
    * The block of the item modifier; at the origin position of the item modifier.
    * The block entity of the item modifier; at the origin position of the item modifier.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [**Identifier**][2] | | The item modifier to apply to the item stack.
`position` | [**Vector**][3] | `{"x": 0, "y": 0, "z": 0}` | If specified, this position will be used for the origin position of the item modifier.
`dimension` | [**Identifier**][2] | `minecraft:overworld` | If specified, this dimension will be used for the origin position of the item modifier.


### Examples

=== "Example #1"

    ```json
    "item_action": {
        "type": "eggolib:modify",
        "modifier": "example:smelt"
    }
    ```

    `data/example/item_modifiers/smelt.json`

    ```json
    {
        "function": "minecraft:furnace_smelt"
    }
    ```

    This example will apply the `example:smelt` item modifier to the item stack, smelting the item stack as if it was smelted in a Furnace.


=== "Example #2"

    ```json
    "item_action": {
        "type": "eggolib:modify",
        "modifier": "example:copy_from_block",
        "position": {
            "x": -30000000,
            "y": 0,
            "z": 1602
        }
    }
    ```

    `data/example/item_modifiers/copy_from_block.json`

    ```json
    {
        "function": "minecraft:copy_nbt",
        "source": "block_entity",
        "ops": [
            {
                "source": "Items",
                "target": "BlockEntityTag.Items",
                "op": "replace"
            }
        ]
    }
    ```

    This example will copy the items from the block container at -30000000 0 1602 in the Overworld to the item stack.



[1]: ../item_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/vector
