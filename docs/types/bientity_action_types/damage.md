---
title: Damage (Bi-entity Action Type)
date: 2022-07-29
search:
    boost: 2
---

#   Damage

**[Bi-entity Action Type]**

Deals damage to the target entity as if the actor entity attacked it.

Type ID: `eggolib:damage`


!!! note

    If the `modifier` field is specified, the max health of the target entity will be used as the base value in the modifier.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`amount` | **[Float]** | *optional* | If specified, this amount of damage will be dealt to the target entity.
`source` | **[Damage Source]** | | Determines the source for the damage to be used. Controls the death message, invulnerabilities or whether armor should be taken into account.
`modifier` | **[Attribute Modifier]** | *optional* | If specified, this modifier and its value will be used as the amount of damage that will be dealt to the target entity.


### Examples

=== "Example #1"

    ``` json
    "bientity_action": {
        "type": "eggolib:damage",
        "amount": 2,
        "source": {
            "name": "generic"
        }
    }
    ```

    This example will deal 2 *(or 1 heart of)* `generic` damage to the target entity.


=== "Example #2"

    ``` json
    "bientity_action": {
        "type": "eggolib:damage",
        "source": {
            "name": "onFire",
            "fire": true
        },
        "modifier": {
            "operation": "multiply_total",
            "value": 0.25
        }
    }
    ```

    This example wil deal 25% `onFire` damage to the target entity. If the max health of the target entity is 20, this example will deal 5 *(2 and a half hearts of)* `onFire` damage.



[Bi-entity Action Type]: ../bientity_action_types.md
[Float]: https://origins.readthedocs.io/en/latest/types/data_types/float
[Damage Source]: https://origins.readthedocs.io/en/latest/types/data_types/damage_source
[Attribute Modifier]: https://origins.readthedocs.io/en/latest/types/data_types/attribute_modifier
