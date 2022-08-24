---
title: Key (Data Types)
date: 2022-08-24
search:
    boost: 2
---

#   Key

**[Data Type]**

An **[object]** or **[string]** used for representing a keybind. This data type is only a placeholder.


### Fields

Fields | Type | Default | Description
-------|------|---------|------------
`key` | **[String]** | | The name of the keybind.


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



[Data Type]: ../data_types.md
[object]: https://origins.readthedocs.io/en/latest/types/data_types/object
[string]: https://origins.readthedocs.io/en/latest/types/data_types/string
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
