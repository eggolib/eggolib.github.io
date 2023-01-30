---
title: Play Sound (Entity Action Type)
date: 2023-01-30
search:
    boost: 2
---

#   Play Sound

[**Entity Action Type**][1]

Plays a sound event at the position of the entity.

Type ID: `eggolib:play_sound`


!!! note

    The value of the `volume` field is used to multiply the base distance of the sound event, which is 16 blocks.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`sound` | [**Identifier**][2] | | The identifier of the sound event to play.
`category` | [**Sound Category**][3] | *optional* | If specified, use this sound category instead of the sound category defined in the entity.
`volume` | [**Float**][4] | `1.0` | The volume of the sound event.
`pitch` | [**Float**][4] | `1.0` | The pitch of the sound event.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:play_sound",
        "sound": "minecraft:entity.creeper.ignite",
        "category": "hostile"
    }
    ```

    This example will play the `minecraft:entity.creeper.ignite` sound event in the `hostile` sound category.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: ../data_types/sound_category.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/float
