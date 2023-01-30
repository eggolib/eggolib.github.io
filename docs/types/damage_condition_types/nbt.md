---
title: NBT (Damage Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   NBT

[**Damage Condition Type**][1]

Checks the NBT of the entity of the damage source.

Type ID: `eggolib:nbt`


!!! warning

    If the damage source does not originate from an entity, then this condition type will evaluate to false.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`nbt` | [**String**][2] |  | The NBT data to check for.


### Examples

=== "Example #1"

    ``` json
    "damage_condition": {
        "type": "eggolib:nbt",
        "nbt": "{Tags: [\"hitter\"]}"
    }
    ```

    This example will check if the entity of the damage source has a `hitter` tag added via the `/tag` command.


=== "Example #2"

    ``` json
    "damage_condition": {
        "type": "apoli:and",
        "conditions": [
            {
                "type": "apoli:projectile",
                "projectile": "minecraft:snowball"
            },
            {
                "type": "eggolib:nbt",
                "nbt": "{Item: {tag: {customProjectile: 1b}}}"
            }
        ]
    }
    ```

    This example will check if the damage source originated from a Snowball projectile that has a `customProjectile` item NBT with a value of `1b`.



[1]: ../damage_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
