---
title: Change Insomnia Ticks (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Change Insomnia Ticks

**[Entity Action Type]**

Changes the value of the `minecraft.custom:minecraft.time_since_rest` statistic of the player.

Type ID: `eggolib:change_insomnia_ticks`


### Fields

Field | Type | Default | Description
------|------|---------|------------
change | **[Integer]** | | The value to be used for changing the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic.
operation | **[String]** | `"add"` | Determines how the specified value will be operated on the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic. Accepts one of `"add"` and `"set"`.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:change_insomnia_ticks",
        "change": 24000,
        "operation": "add"
    }
    ```

    This example will add 24000 to the the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic, essentially adding 1 day.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:change_insomnia_ticks",
        "change": 0,
        "operation": "set"
    }
    ```

    This example will set the the value of the player's `minecraft.custom:minecraft.time_since_rest` statistic to 0.



[Entity Action Type]: ../entity_action_types.md
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
