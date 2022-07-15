---
title: Modify Hurt Ticks (Power Types)
date: 2022-07-14
search:
    boost: 1
---

#   Modify Hurt Ticks

**[Power Type]**

Modifies how long the entity that has the power is immune to damage upon being damaged.

Type ID: `eggolib:modify_hurt_ticks`


!!! note

    By default, an entity has a "hurt ticks" value of 20. The entity will only receive damage again only if either their "hurt ticks" value is less than 10 or if they receive a damage with a higher value than the previous.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | **[Bi-entity Action Type]** | *optional* | If specified, this action will be executed on either or both the actor or target entities.
`bientity_condition` | **[Bi-entity Condition Type]** | *optional* | If specified, the specified action/modifier(s) will only be executed/applied if this condition is fulfilled by either or both actor or target entities.
`damage_condition` | **[Damage Condition Type]** | *optional* | If specified, the specified action/modifier(s) will only be executed/applied if this condition is fulfilled by the damage dealt to the target entity.
`modifier` | **[Attribute Modifier]** | *optional* | If specified, this modifier will be applied to the hurt ticks of the target entity.
`modifiers` | **[Array]** of **[Attribute Modifiers]** | *optional* | If specified, these modifiers will be applied to the hurt ticks of the target entity.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_hurt_ticks",
        "modifier": {
            "operation": "multiply_total",
            "value": 1
        }
    }
    ```

    This example will double the hurt ticks of the entity that has the power.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:modify_hurt_ticks",
        "damage_condition": {
            "type": "apoli:attacker"
        },
        "modifier": {
            "operation": "multiply_total",
            "value": -0.5
        }
    }
    ```

    This example will half the hurt ticks of the entity that has the power only if the entity has been attacked by another entity.



[Power Type]: ../power_types.md
[Bi-entity Action Type]: https://origins.readthedocs.io/en/latest/types/bientity_action_types
[Bi-entity Condition Type]: https://origins.readthedocs.io/en/latest/types/bientity_condition_types
[Damage Condition Type]: ../damage_condition_types.md
[Attribute Modifier]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[Attribute Modifiers]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
