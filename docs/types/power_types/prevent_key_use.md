---
title: Prevent Key Use (Power Type)
date: 2023-06-18
search:
    boost: 2
---

#   Prevent Key Use

[**Power Type**][1]

Prevents the entity from pressing certain keybinds.

Type ID: `eggolib:prevent_key_use`


!!! note

    This power type will only work for players.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`key` | [**Functional Key**][2] | *optional* | If specified, this key will be prevented from being pressed.
`keys` | [**Array**][3] of [**Functional Keys**][2] | *optional* | If specified, these keys will be prevented from being pressed.


### Examples

=== "Example #1"

    ```json
    {
        "type": "eggolib:prevent_key_use",
        "key": "key.inventory"
    }
    ```

    This example will prevent the entity that has the power from pressing the `key.inventory` keybind, therefore preventing the entity from accessing their inventory.


=== "Example #2"

    ```json
    {
        "type": "eggolib:prevent_key_use",
        "keys": [
            "key.hotbar.1",
            {
                "key": "key.jump",
                "action": {
                    "type": "apoli:execute_command",
                    "command": "title @s actionbar {\"text\": \"You cannot jump!\", \"color\": \"red\"}"
                }
            }
        ]
    }
    ```

    This example will prevent the entity from pressing the `key.hotbar.1` keybind and the `key.jump` keybind with a `"You cannot jump!"` red-colored message.



[1]: ../power_types.md
[2]: ../data_types/functional_key.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
