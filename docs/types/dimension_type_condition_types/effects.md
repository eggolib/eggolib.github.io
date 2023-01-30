---
title: Effects (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Effects

[**Dimension Type Condition Type**][1]

Checks if the identifier of the effects of the dimension matches the specified identifier.

Type ID: `eggolib:effects`


!!! note

    See [Minecraft Fandom Wiki: Effect (dimension)](https://minecraft.fandom.com/wiki/Effect_(dimension)) for more information about dimension effects.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`id` | [**Identifier**][2] | | The identifier of the dimension effects property to check for.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:effects",
        "id": "minecraft:the_end"
    }
    ```

    This example will check if the dimension has The End dimension's effects.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
