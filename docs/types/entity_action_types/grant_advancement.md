---
title: Grant Advancement (Entity Action Type)
date: 2023-07-06
search:
    boost: 2
---

#   Grant Advancement

[**Entity Action Type**][1]

Grants an advancement or a criterion/criteria of an advancement to the player.

Type ID: `eggolib:grant_advancement`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`advancement` | [**Identifier**][2] | _optional_ | The advancement to grant to the player.
`criterion` | [**String**][3] | _optional_ | If specified, this criterion will be granted to the player.
`criteria` | [**Array**][4] of [**Strings**][3] | _optional_ | If specified, these criteria will be granted to the player.
`selection` | [**Advancement Selection**][5] | `"only"` | Determines how the parent(s) and child(ren) of the specified advancement is granted.


### Examples

=== "Example #1"

    ```json
    "entity_action": {
        "type": "eggolib:grant_advancement",
        "selection": "everything"
    }
    ```

    This example will grant all the advancements to the player.


=== "Example #2"

    ```json
    "entity_action": {
        "type": "eggolib:grant_advancement",
        "advancement": "minecraft:story/obtain_armor"
    }
    ```

    This example will grant the "Suit Up" (`data/minecraft/advancements/story/obtain_armor.json`) advancement to the player.


=== "Example #3"

    ```json
    "entity_action": {
        "type": "eggolib:grant_advancement",
        "advancement": "minecraft:adventure/kill_all_mobs",
        "criteria": [
            "minecraft:blaze",
            "minecraft:enderman",
            "minecraft:zombie"
        ]
    }
    ```

    This example will grant the "Monsters Hunted" (`data/minecraft/advancements/adventure/kill_all_mobs.json`) advancement partially, with only the `minecraft:blaze`, `minecraft:enderman`, and `minecraft:zombie` criteria fulfilled.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
[4]: https://origins.readthedocs.io/en/latest/types/data_types/array
[5]: ../data_types/advancement_selection.md
