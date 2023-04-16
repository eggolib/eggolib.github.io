---
title: Modify FOV (Power Type)
date: 2023-04-16
search:
    boost: 2
---

#   Modify FOV

[**Power Type**][1]

Modifies the field of view of the entity that has the power.

Type ID: `eggolib:modify_fov`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [**Attribute Modifier**][2] | *optional* | If specified, this modifier will be applied to the field of view of the entity that has the power.
`modifiers` | [**Array**][3] of [**Attribute Modifiers**][2] | *optional* | If specified, these modifiers will be applied to the field of view of the entity that has the power.
`affected_by_fov_effect_scale` | [**Boolean**][4] | `true` | Determines whether the field of view is affected by the "FOV Effects" accessibility option.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_fov",
        "modifier": {
            "operation": "multiply_total_multiplicative",
            "value": -0.25
        }
    }
    ```

    This example will reduce the field of view of the entity by 25%.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:modify_fov",
        "modifier": {
            "operation": "multiply_total_multiplicative",
            "value": 0.75
        },
        "affected_by_fov_effects_scale": false
    }
    ```

    This example will increase the field of view of the entity by 75%, which also won't be affected by the "FOV Effects" accessibility option.



[1]: ../power_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
[4]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
