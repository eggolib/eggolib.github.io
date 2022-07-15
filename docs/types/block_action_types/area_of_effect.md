---
title: Area of Effect (Block Action Type)
date: 2022-07-14
search:
    boost: 1
---

#   Area of Effect

**[Block Action Type]**

Executes an action on blocks that are within the specified radius.

Type ID: `eggolib:area_of_effect`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`radius` | **[Integer]** | | Determines the radius of the area to execute the action on.
`shape` | **[String]** | `"cube"` | Determines the shape of the area to execute the action on. Accepts one of `"cube"`, `"star"` or `"sphere"`.
`block_action` | **[Block Action Type]** | | The action to execute on the block(s) within the specified radius.
`block_condition` | **[Block Condition Type]** | *optional* | If specified, only execute the specified action on the block(s) that fulfills this condition.


### Examples

=== "Example #1"

    ``` json
    "block_action": {
        "type": "eggolib:area_of_effect",
        "radius": 16,
        "shape": "cube",
        "block_action": {
            "type": "apoli:modify_block_state",
            "property": "waterlogged",
            "value": false
        }
    }
    ```

    This example will make all waterloggable blocks not waterlogged within 16 blocks radius with a shape of a cube.


=== "Example #2"

    ``` json
    "block_action": {
        "type": "eggolib:area_of_effect",
        "radius": 4,
        "shape": "star",
        "block_action": {
            "type": "apoli:set_block",
            "block": "minecraft:air"
        },
        "block_condition": {
            "type": "apoli:in_tag",
            "tag": "minecraft:dragon_immune",
            "inverted": true
        }
    }
    ```

    This example will replace all blocks that aren't included in the `#minecraft:dragon_immune` block tag with Air within a 4 blocks radius with a shape of a star.



[Block Action Type]: ../block_action_types.md
[Integer]: https://origins.readthedocs.io/en/1.4.1/types/data_types/integer
[String]: https://origins.readthedocs.io/en/1.4.1/types/data_types/string
[Block Condition Type]: ../block_condition_types.md
