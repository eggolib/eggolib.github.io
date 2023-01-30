---
title: Modify Label Render (Power Type)
date: 2022-01-30
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
`render_mode` | [**Render Mode**][2] | `"default"` | Determines how the name label of the entity is rendered.
`text` | [**Text Component**][3] | *optional* | If specified, this text will be used to replace the content of the name label of the entity.
`priority` | [**Integer**][4] | `0` | Determines the priority of the power. The power with the highest value will be used.


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



[1]: ../power_types.md
[2]: ../data_types/render_mode.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/text_component
[4]: https://origins.readthedocs.io/en/latest/types/data_types/integer
