---
title: Permission Level (Entity Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   Permission Level

[**Entity Condition Type**][1]

Checks if the entity has the specified permission level.

Type ID: `eggolib:permission_level`

!!! caution

    This may not work properly in singleplayer.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | `">="` | Determines how the permission level of the entity should be compared to the specified value.
`compare_to` | [**Integer**][3] | `2` | The value which the permission level of the entity should be compared to.


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



[1]: ../entity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
