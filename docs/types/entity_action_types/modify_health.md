---
title: Modify Health (Entity Action Type)
date: 2022-07-29
search:
    boost: 2
---

#   Modify Health

[**Entity Action Type**][1]

Modifies the current health of the entity.

Type ID: `eggolib:modify_health`


!!! note

    The max health of the entity will be used as the base value for the modifier.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`modifier` | [**Attribute Modifier**][2] | | The modifier to use for modifying the current health of the entity.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_health",
        "modifier": {
            "operation": "add_base_early",
            "value": -2
        }
    }
    ```

    This example will subtract 2 *(or 1 heart)* from the entity's current health.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_health",
        "modifier": {
            "operation": "multiply_total",
            "value": -0.25
        }
    }
    ```

    This example will subtract 25% from the entity's current health. If the max health of the entity is 20, this example will subtract 5 *(or 2 and a half hearts)* from the entity's current health.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
