---
title: Type (Damage Condition Type)
date: 2023-07-07
search:
    boost: 2
---

#   Type

[**Damage Condition Type**][1]

Checks whether the damage source is of a certain damage type.

Type ID: `eggolib:type`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`damage_type` | [**Identifier**][2] | | The identifier of the damage type to compare the damage source to.


### Examples

=== "Example #1"

    ```json
    "damage_condition": {
        "type": "eggolib:type",
        "damage_type": "minecraft:lightning_bolt"
    }
    ```

    This example will check if the damage source is of the `minecraft:lightning_bolt` damage type.


=== "Example #2"

    ```json
    "damage_condition": {
        "type": "eggolib:type",
        "damage_type": "eggolib:change_health_underflow"
    }
    ```

    This example will check if the damage source is of the `eggolib:change_health_underflow` damage type, which is dealt by the [**Change Health (Entity Action Type)**][3] and the [**Modify Health (Entity Action Type)**][4] if the new health value is < 0.



[1]: ../damage_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: ../entity_action_types/change_health.md
[4]: ../entity_action_types/modify_health.md
