---
title: Permission Level (Entity Condition Types)
date: 2022-07-14
---

#   Permission Level

**[Entity Condition Type]**

Checks if the entity has the specified permission level.

Type ID: `eggolib:permission_level`

!!! caution

    This may not work properly in singleplayer.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | **[Comparison]** | `">="` | Determines how the permission level of the entity should be compared to the specified value.
`compare_to` | **[Integer]** | `2` | The value which the permission level of the entity should be compared to.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:permission_level",
        "comparison": ">=",
        "compare_to": 1
    }
    ```

    This example will check if the entity is opped in general.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:permission_level",
        "comparison": "==",
        "compare_to": 4
    }
    ```

    This example will check if the entity has a permission level of 4, which is the highest permission level.



[Entity Condition Type]: ../entity_condition_types.md
[Comparison]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer
