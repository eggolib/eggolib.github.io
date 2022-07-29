---
title: Block Collision (Entity Condition Type)
date: 2022-07-29
search:
    boost: 2
----

#   Block Collision

**[Entity Condition Type]**

Checks whether the bounding box of the entity is colliding with a block.

Type ID: `eggolib:block_collision`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_condition` | **[Block Condition Type]** | *optional* | If specified, the condition will only evaluate to true if this condition is fulfilled by the block colliding with the bounding box of the entity.
`offset_x` | **[Float]** | `0` | Determines the offset for the bounding box of the entity in the X axis.
`offset_y` | **[Float]** | `0` | Determines the offset for the bounding box of the entity in the Y axis.
`offset_z` | **[Float]** | `0` | Determines the offset for the bounding box of the entity in the Z axis.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:block_collision",
        "offset_x": 0.1,
        "offset_z": 0.1
    }
    ```

    This example will check if the bounding box of the entity is colliding with the east and south faces of a block.


=== "Example #2"

    ``` json
    "condition": {
        "type": "apoli:or",
        "conditions": [
            {
                "type": "eggolib:block_collision",
                "block_condition": {
                    "type": "apoli:block",
                    "block": "minecraft:white_wool"
                },
                "offset_x": 0.01,
                "offset_z": 0.01
            },
            {
                "type": "eggolib:block_collision",
                "block_condition": {
                    "type": "apoli:block",
                    "block": "minecraft:white_wool"
                },
                "offset_x": -0.01,
                "offset_z": -0.01
            }
        ]
    }
    ```

    This example will check if the bounding box of the entity is colliding with the north, south, east or west faces of a White Wool block.



[Entity Condition Type]: ../entity_condition_types.md
[Block Condition Type]: ../block_condition_types.md
[Float]: https://origins.readthedocs.io/en/latest/types/data_types/float
