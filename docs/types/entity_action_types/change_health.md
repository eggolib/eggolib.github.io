---
title: Change Health (Entity Action Types)
date: 2022-07-14
search:
    boost: 1
---

#   Change Health

**[Entity Action Type]**

Changes the health of the entity.

Type ID: `eggolib:change_health`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`change` | **[Float]** | | The value to be used for modifying the entity's health.
`operation` | **[String]** | `"add"` | Determines how the specified value will be operated on the entity's health. Accepts one of `"add"` and `"set"`.


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



[Entity Action Type]: ../entity_action_types.md
[Float]: https://origins.readthedocs.io/en/1.4.1/types/data_types/float
[String]: https://origins.readthedocs.io/en/1.4.1/types/data_types/string
