---
title: Projectile (Damage Condition Types)
date: 2022-07-14
---

#   Projectile

**[Damage Condition Type]**

Checks whether the damage source is projectile damage; can also optionally check the type(s) of projectile or its NBT.

Type ID: `eggolib:projectile`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`projectile` | **[Identifier]** | *optional* | If specified, the condition will evaluate to true if the projectile matches this entity type identifier.
`projectiles` | **[Array]** of **[Identifiers]** | *optional* | If specified, the condition will evaluate to true if the projectile matches any of these entity type identifiers.
`nbt` | **[String]** | *optional* | If specified, the condition will evaluate to true if the projectile has this NBT data.


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



[Damage Condition Type]: ../damage_condition_types.md
[Identifier]: https://origins.readthedocs.io/en/1.4.1/types/data_types/identifier
[Identifiers]: https://origins.readthedocs.io/en/1.4.1/types/data_types/identifier
[Array]: https://origins.readthedocs.io/en/1.4.1/types/data_types/array
[String]: https://origins.readthedocs.io/en/1.4.1/types/data_types/string
