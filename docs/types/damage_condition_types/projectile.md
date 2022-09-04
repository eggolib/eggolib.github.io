---
title: Projectile (Damage Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   Projectile

[**Damage Condition Type**][1]

Checks whether the damage source is projectile damage; can also optionally check the type(s) of projectile or its NBT.

Type ID: `eggolib:projectile`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`projectile` | [**Identifier**][2] | *optional* | If specified, the condition will evaluate to true if the projectile matches this entity type identifier.
`projectiles` | [**Array**][3] of [**Identifiers**][2] | *optional* | If specified, the condition will evaluate to true if the projectile matches any of these entity type identifiers.
`nbt` | [**String**][4] | *optional* | If specified, the condition will evaluate to true if the projectile has this NBT data.


### Examples

=== "Example #1"

    ``` json
    "damage_condition": {
        "type": "eggolib:projectile",
        "nbt": "{Item: {tag: {heavyProjectile: 1b}}}"
    }
    ```

    This example will check if the damage source is of a projectile that has the `{Item: {tag: {heavyProjectile: 1b}}}` NBT.


=== "Example #2"

    ``` json
    "damage_condition": {
        "type": "eggolib:projectile",
        "projectiles": [
            "minecraft:arrow",
            "minecraft:spectral_arrow",
            "minecraft:snowball",
            "minecraft:llama_spit"
        ]
    }
    ```

    This example will check if the damage source is of a projectile that's either an Arrow, a Spectral Arrow, a Snowball or a Llama Spit.



[1]: ../damage_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
[4]: https://origins.readthedocs.io/en/latest/types/data_types/string
