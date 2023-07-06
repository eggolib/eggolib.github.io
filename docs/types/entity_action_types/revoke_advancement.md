---
title: Revoke Advancement (Entity Action Type)
date: 2023-07-06
search:
    boost: 2
---

#   Revoke Advancement

[**Entity Action Type**][1]

Revokes an advancement or a criterion/criteria of an advancement from the player.

Type ID: `eggolib:grant_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`advancement` | [**Identifier**][2] | _optional_ | The advancement to revoke from the player.
`criterion` | [**String**][3] | _optional_ | If specified, this criterion will be revoked from the player.
`criteria` | [**Array**][4] of [**Strings**][3] | _optional_ | If specified, these criteria will be revoked from the player.
`selection` | [**Advancement Selection**][5] | `"only"` | Determines how the parent(s) and child(ren) of the specified advancement is revoked.


### Examples

=== "Example #1"

    ```json
    "entity_action": {
        "type": "eggolib:revoke_advancement",
        "selection": "everything"
    }
    ```

    This example will revoke all the advancements from the player.


=== "Example #2"

    ```json
    "entity_action": {
        "type": "eggolib:grant_advancement",
        "advancement": "minecraft:story/mine_stone"
    }
    ```

    This example will revoke the "Stone Age" (`data/minecraft/advancements/story/mine_stone.json`) advancement from the player.


=== "Example #3"

    ```json
    "entity_action": {
        "type": "eggolib:grant_advancement",
        "advancement": "minecraft:adventure/adventuring_time",
        "criteria": [
            "minecraft:badlands",
            "minecraft:beach",
            "minecraft:desert"
        ]
    }
    ```

    This example will revoke the "Adventuring Time" (`data/minecraft/advancements/adventure/adventuring_time.json`) advancement partially, with only the `minecraft:badlands`, `minecraft:beach`, and `minecraft:desert` criteria revoked.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
[4]: https://origins.readthedocs.io/en/latest/types/data_types/array
[5]: ../data_types/advancement_selection.md
