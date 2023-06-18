---
title: Command (Block Condition Type)
date: 2023-06-18
search:
    boost: 2
---

#   Command

[**Block Condition Type**][1]

Compares the result of the specified command to the specified value.

Type ID: `eggolib:command`


!!! caution

    This block condition type is only effective server-side. This means that client-side power types won't be able to evaluate this properly.


### Fields

Field | Type | Default | Description
------|------|---------|------------
command | [**String**][2] | | The command to execute.
comparison | [**Comparison**][3] | `">="` | Determines how the result of the command is compared to a value.
compare_to | [**Integer**][4] | `1` | The value to compare the result of the command to.


### Examples

=== "Example #1"

    ```json
    "block_condition": {
        "type": "eggolib:command",
        "command": "execute if entity @e[type = minecraft:creeper, distance = ..4]"
    }
    ```

    This example will check if there are 1 or more Creepers at the position of the block the block condition type is evaluated on.



[1]: ../block_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
[3]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[4]: https://origins.readthedocs.io/en/latest/types/data_types/integer
