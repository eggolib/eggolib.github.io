---
title: In Screen (Entity Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   In Screen

**[Entity Condition Type]**

Checks if the player has any or specific screen open.

Type ID: `eggolib:in_screen`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`screen` | **[String]** | *optional* | If specified, the condition will evaluate to true if the player's current screen matches this screen. See **[In-Game Screen Class (Class Data Registry)]** for possible values.
`screens` | **[Array]** of **[Strings]** | *optional* | If specified, the condition will evaluate to true if the player's current screen matches any of these screens. See **[In-Game Screen Class (Class Data Registry)]** for possible values.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:in_screen"
    }
    ```

    This example will check if the player has a screen open.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:in_screen",
        "screens": [
            "inventory",
            "creative_inventory"
        ]
    }
    ```

    This example will check if the player has the inventory or creative inventory screen open.


[Entity Condition Type]: ../entity_condition_types.md
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Strings]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[In-Game Screen Class (Class Data Registry)]: ../../misc/class_data_registries/in-game_screen_class.md
