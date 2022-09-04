---
title: Change Health (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Change Health

[**Entity Action Type**][1]

Changes the health of the entity.

Type ID: `eggolib:change_health`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`change` | [**Float**][2] | | The value to be used for modifying the entity's health.
`operation` | [**String**][3]] | `"add"` | Determines how the specified value will be operated on the entity's health. Accepts one of `"add"` and `"set"`.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:change_health",
        "change": 1,
        "operation": "add"
    }
    ```

    This example will add 1 to the entity's health.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:change_health",
        "change": 10,
        "operation": "set"
    }
    ```

    This example will set the entity's health to 10.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/float
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
