---
title: Modify Label Render (Power Type)
date: 2023-01-30
search:
    boost: 2
---

#   Modify Label Render

[**Power Type**][1]

Modifies the name label of the entity that has the power.

Type ID: `eggolib:modify_label_render`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`before_parse_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed on the entity **before** the `text` is parsed.
`after_parse_action` | [**Entity Action Type**][2] | *optional* | If specified, this action will be executed on the entity **after** the `text` is parsed and if the parsed text is not the same as it was previously.
`render_mode` | [**Render Mode**][3] | `"default"` | Determines how the name label of the entity is rendered.
`text` | [**Text Component**][4] | *optional* | If specified, this text will be parsed to replace the content of the name label of the entity.
`tick_rate` | [**Positive Integer**][5] | `20` | Determines the interval at which the action(s) is/are executed and the `text` is parsed.
`priority` | [**Integer**][6] | `0` | Determines the priority of the power. The power with the highest value will be used.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:modify_label_render",
        "render_mode": "hide_partially"
    }
    ```

    This example will render the name label of the entity semi-transparently as if the entity is sneaking.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:modify_label_render",
        "text": {
            "text": "[REDACTED]",
            "bold": true,
            "color": "black"
        }
    }
    ```

    This example will replace the content of the name label of the entity to `[REDACTED]` with the color black.


=== "Example #3"

    ``` json
    {
        "type": "eggolib:modify_label_render",
        "text": [
            {
                "text": "[",
                "color": "yellow"
            },
            {
                "selector": "@s",
                "color": "green",
                "bold": true
            },
            {
                "text": "]",
                "color": "yellow"
            }
        ]
    }
    ```

    This example will replace the contents of the name label of the entity to have its name (with the use of the `selector` JSON text component) colored green and surround it with yellow-colored brackets



[1]: ../power_types.md
[2]: ../entity_action_types.md
[3]: ../data_types/render_mode.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/text_component
[5]: ../data_types/positive_integer.md
[6]: https://origins.readthedocs.io/en/latest/types/data_types/integer
