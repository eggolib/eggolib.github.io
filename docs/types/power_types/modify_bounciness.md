---
title: Modify Bounciness (Power Type)
date: 2023-01-31
search:
    boost: 2
---

#   Modify Bounciness

[**Power Type**][1]

Modifies the bounciness of the block the entity has landed on.

Type ID: `eggolib:modify_bounciness`


!!! note

    The base value for reducing the velocity of the entity upon bouncing is 0.8, which is later inverted to negative.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed on the entity upon bouncing.
`block_action` | [**Block Action Type**][3] | *optional* | If specified, this action will be executed on the block the entity landed on.
`block_condition` | [**Block Condition Type**][4] | *optional* | If specified, only blocks that fulfill this condition will have its bounciness modified.
`modifier` | [**Attribute Modifier**][5] | *optional* | If specified, this modifier will be applied on the value used for reducing the velocity of the entity upon bouncing.
`modifiers` | [**Array**][6] of [**Attribute Modifiers**][5] | *optional* | If specified, these modifiers will be applied on the value used for reducing the velocity of the entity upon bouncing.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_bounciness",
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:sponge"
        }
    }
    ```

    This example will make Sponge blocks bouncy like Slime blocks.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:modify_bounciness",
        "block_action": {
            "type": "apoli:set_block",
            "block": "minecraft:sand"
        },
        "block_condition": {
            "type": "apoli:block",
            "block": "minecraft:gravel"
        }
    }
    ```

    This example will make Gravel blocks bouncy like Slime blocks, while also replacing the Gravel block the entity has landed on with a Sand block.



[1]: ../power_types.md
[2]: ../entity_action_types.md
[3]: ../block_action_types.md
[4]: ../block_condition_types.md
[5]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[6]: https://origins.readthedocs.io/en/latest/types/data_types/array
