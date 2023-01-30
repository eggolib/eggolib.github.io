---
title: Modify Mouse Sensitivity (Power Type)
date: 2023-01-31
search:
    boost: 2
---

#   Modify Mouse Sensitivity

[**Power Type**][1]

Modifies the sensitivity of the player's mouse.

Type ID: `eggolib:modify_mouse_sensitivity`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [**Attribute Modifier**][2] | *optional* | If specified, this modifier will be applied to the sensitivity of the player's mouse.
`modifiers` | [**Array**][3] of [**Attribute Modifiers**][2] | *optional* | If specified, these modifiers will be applied to the sensitivity of the player's mouse.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_mouse_sensitivity",
        "modifier": {
            "operation": "multiply_total_multiplicative",
            "value": -0.5
        }
    }
    ```

    This example will decrease the sensitivity of the player's mouse by 50%.



[1]: ../power_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
