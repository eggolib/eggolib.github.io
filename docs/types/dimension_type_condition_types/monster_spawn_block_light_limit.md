---
title: Monster Spawn Block Light Limit (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Monster Spawn Block Light Limit

[**Dimension Type Condition Type**][1]

Compares the maximum required block light for spawning mobs of the dimension to the specified value.

Type ID: `eggolib:monster_spawn_block_light_limit`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the maximum required block light for spawning mobs of the dimension is compared to the specified value.
`compare_to` | [**Integer**][3] | | The value which the maximum required block light for spawning mobs of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:monster_spawn_block_light_limit",
        "comparison": "==",
        "compare_to": 0
    }
    ```

    This example will check if the maximum required block light for spawning mobs in the dimension is 0. For instance, the Overworld dimension fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
