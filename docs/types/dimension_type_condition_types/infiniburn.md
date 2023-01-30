---
title: Infiniburn (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Infiniburn

[**Dimension Type Condition Type**][1]

Checks if the dimension is using the specified block tag for setting blocks on fire forever until extinguished manually.

Type ID: `eggolib:infiniburn`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`tag` | [**Identifier**][2] | | The identifier of the block tag to check for.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:infiniburn",
        "tag": "minecraft:infiniburn_overworld"
    }
    ```

    This example will check if the dimension is using the `#minecraft:infiniburn_overworld` block tag for blocks that burn forever.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
