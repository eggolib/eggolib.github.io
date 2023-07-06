---
title: Tooltip (Power Type)
date: 2023-06-07
search:
    boost: 2
---

#   Tooltip

[**Power Type**][1]

Applies the specified tooltip text(s) to an item that is only visible to the entity that has the power.

Type ID: `eggolib:tooltip`


!!! note

    This power type allows for usage of JSON text components that require "resolving". See [**Minecraft Fandom Wiki: Raw JSON text format (Component resolution)**][2] for more information.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`item_condition` | [**Item Condition Type**][3] | _optional_ | If specified, the specified tooltip text(s) will only apply to items that fulfill this condition.
`text` | [**Text Component**][4] | _optional_ | If specified, this tooltip text will be applied to the item.
`texts` | [**Array**][5] of [**Text Components**][4] | _optional_ | If specified, these tooltip texts will be applied to the item.
`tick_rate` | [**Positive Integer**][6] | `20` | Determines how frequent the specified tooltip text(s) are resolved.
`order` | [**Integer**][7] | `0` | Determines the placement order of the tooltip text(s) of the power.


### Examples

=== "Example #1"

    ```json
    {
        "type": "eggolib:tooltip",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "item": "minecraft:diamond"
            }
        },
        "text": {
            "text": "Ooh, shiny!",
            "color": "yellow"
        }
    }
    ```

    This example will apply a yellow-colored `"Ooh, shiny!"` tooltip text to Diamond items.


=== "Example #2"

    ```json
    {
        "type": "eggolib:tooltip",
        "item_condition": {
            "type": "apoli:ingredient",
            "ingredient": {
                "tag": "example:melee_weapons"
            }
        },
        "text": [
            "",
            {
                "text": "Kills: ",
                "color": "gray",
                "italic": false
            },
            {
                "score": {
                    "name": "@s",
                    "objective": "melee_kills"
                },
                "color": "red",
                "bold": true
            }
        ]
    }
    ```

    This example will apply a gray-colored `"Kills: <number>"` tooltip text to items that are included in the `#example:melee_weapons` (`data/example/tags/items/melee_weapons.json`) item tag.

    With `<number>` being the score of the entity that has the power from the `melee_kills` scoreboard objective colored red and bold.



[1]: ../power_types.md
[2]: https://minecraft.fandom.com/wiki/Raw_JSON_text_format#Component_resolution
[3]: ../item_condition_types.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/text_component
[5]: https://origins.readthedocs.io/en/latest/types/data_types/array
[6]: ../data_types/positive_integer.md
[7]: https://origins.readthedocs.io/en/latest/types/data_types/integer
