---
title: Spawn Entity
date: 2023-01-30
search:
    boost: 2
---

#   Spawn Entity

[**Entity Action Type**][1]

Spawns an entity.

Type ID: `eggolib:spawn_entity`


!!! note

    This action type can spawn in entities with passengers.


### Field

Field | Type | Default | Description
------|------|---------|------------
`entity_type` | [**Identifier**][2] | | The identifier of the entity that will be spawned.
`tag` | [**String**][3] | *optional* | If specified, this NBT data will be added to the entity that will be spawned.
`entity_action` | [**Entity Action Type**][1] | *optional* | If specified, this action will be executed on the entity that will be spawned.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:spawn_entity",
        "entity_type": "minecraft:skeleton",
        "tag": "{ArmorItems: [{}, {}, {}, {id: \"minecraft:iron_helmet\", Count: 1b}]}"
    }
    ```

    This example will spawn a Skeleton with an Iron Helmet.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:spawn_entity",
        "entity_type": "minecraft:skeleton_horse",
        "tag": "{Passengers: [{id: \"minecraft:skeleton\", ArmorItems: [{}, {}, {}, {id: \"minecraft:golden_helmet\", Count: 1b}]}]}"
    }
    ```

    This example will spawn a Skeleton Horse with a Skeleton passenger equipped with a Golden Helmet.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
