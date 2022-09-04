---
title: Breaking Block (Entity Condition Type)
date: 2022-09-04
search:
    boost: 2
---

#   Breaking Block

[**Entity Condition Type**][1]

Checks if the player is currently breaking a block.

Type ID: `eggolib:breaking_block`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`block_condition` | [**Block Condition Type**][2] | *optional* | If specified, the condition will only evaluate to true if this condition is fulfilled by the block being broken.
`using_effective_tool` | [**Boolean**][3] | `false` | Determines if the condition should check if the player is using the effective tool for the block being broken.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:breaking_block",
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:diamond_block"
        }
    }
    ```

    This example will check if the player is currently mining a Diamond Block.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:breaking_block",
        "using_effective_tool": true
    }
    ```
    
    This example will check if the player is currently mining a block using its effective tool.



[1]: ../entity_condition_types.md
[2]: ../block_condition_types.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
