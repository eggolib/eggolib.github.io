---
title: Functional Key (Data Types)
date: 2022-08-24
search:
    boost: 2
---

#   Functional Key

**[Data Type]**

An **[object]** or **[string]** used for representing a keybind. If formatted as an **[object]**, this data type can execute **[Entity Action Types]**.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`key` | **[String]** | | The name of the keybind.
`continuous` | **[Boolean]** | `false` | Determines if the keybind can be pressed continuously if held.
`action` | **[Entity Action Type]** | *optional* | If specified, this action will be executed on the player upon pressing the specified keybind.


### Examples

=== "Example #1"

    ``` json
    "keys": [
        "key.forward"
    ]
    ```

    This example represents the `key.forward` keybind, with its `continuous` and `action` fields having its default values:  `false` and `null` respectively.


=== "Example #2"

    ``` json
    "keys": [
        {
            "key": "key.jump",
            "continuous": false,
            "action": {
                "type": "apoli:execute_command",
                "command": "me jumped!"
            }
        }
    ]
    ```

    This example represents the `key.jump` keybind. Upon pressing the specified keybind, this will execute a `/me jumped!` command.



[Data Type]: ../data_types.md
[object]: https://origins.readthedocs.io/en/latest/types/data_types/object
[string]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Entity Action Types]: ../entity_action_types.md
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Boolean]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
[Entity Action Type]: ../entity_action_types.md
