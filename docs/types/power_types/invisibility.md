---
title: Invisibility (Power Types)
date: 2022-07-14
search:
    boost: 2
---

#   Invisibility

**[Power Type]**

Grants the entity that has the power invisibility, which may or may not affect their armor.

Type ID: `eggolib:invisibility`


!!! note

    In the context of this power type, the '**target**' entity is the entity that has the power whilst the '**actor**' entities are the players that can see the '**target**' entity.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_condition` | **[Bi-entity Condition Type]** | *optional* | If specified, the '**target**' entity will only be invisible to the '**actor**' entities if this condition is fulfilled by either or both '**actor**' and '**target**' entities.
`render_armor` | **[Boolean]** | | Determines if the armor should also be invisible.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:invisibility",
        "render_armor": false
    }
    ```

    This example will make the entity that has the power invisible to all entities.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:invisibility",
        "bientity_condition": {
            "type": "apoli:actor_condition",
            "condition": {
                "type": "apoli:power",
                "power": "*:*"
            },
            "inverted": true
        },
        "render_armor": false
    }
    ```

    This example will make the entity that has the power invisible to entities. The entity will also be invisible to players that do not have the power.



[Power Type]: ../power_types.md
[Bi-entity Condition Type]: https://origins.readthedocs.io/en/latest/types/bientity_condition_types
[Boolean]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
