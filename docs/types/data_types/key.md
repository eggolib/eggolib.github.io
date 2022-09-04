---
title: Key (Data Type)
date: 2022-08-24
search:
    boost: 2
---

#   Key

[**Data Type**][1]

An [**object**][2] or [**string**][3] used for representing a keybind. This data type is only a placeholder.


### Fields

Fields | Type | Default | Description
-------|------|---------|------------
`key` | [**String**][3] | | The name of the keybind.


### Examples

=== "Example #1"

    ``` json
    "keys": [
        "key.attack"
    ]
    ```

    This example represents the `key.attack` keybind.


=== "Example #2"

    ``` json
    "keys": [
        {
            "key": "key.jump"
        }
    ]
    ```

    This example represents the `key.jump` keybind.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/object
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
