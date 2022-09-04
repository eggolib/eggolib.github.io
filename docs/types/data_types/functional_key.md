---
title: Functional Key (Data Type)
date: 2022-08-24
search:
    boost: 2
---

#   Functional Key

[**Data Type**][1]

An [**object**][2] or [**string**][3] used for representing a keybind. If formatted as an [**object**][2], this data type can execute an [**Entity Action Type**][4].


### Fields

Field | Type | Default | Description
------|------|---------|------------
`key` | [**String**][3] | | The name of the keybind.
`continuous` | [**Boolean**][5] | `false` | Determines if the keybind can be pressed continuously if held.
`action` | [**Entity Action**][4] | *optional* | If specified, this action will be executed on the player upon pressing the specified keybind.


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



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/object
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
[4]: ../entity_action_types.md
[5]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
