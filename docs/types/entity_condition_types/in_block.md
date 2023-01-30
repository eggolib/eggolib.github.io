---
title: In Block (Entity Condition Type)
date: 2022-01-31
search:
    boost: 2
---

#   In Block

[**Entity Condition Type**][1]

Checks if the entity's feet or eyes is in a block.

Type ID: `eggolib:in_block`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_condition` | [**Block Condition Type**][2] | | The condition to test on the block at the entity's specified offset.
`offset` | [**Entity Offset**][3] | `"feet"` | Determines the offset of where the condition should check for the block.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:in_block",
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:water"
        }
    }
    ```

    This example will check if the entity's feet is in water.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:in_block",
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:lava"
        },
        "offset": "eyes"
    }
    ```

    This example will check if the entity's eyes is in lava.



[1]: ../entity_condition_types.md
[2]: ../block_condition_types.md
[3]: ../data_types/entity_offset.md
