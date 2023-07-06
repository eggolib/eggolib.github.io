---
title: Execute Command (Item Action Type)
date: 2023-07-06
search:
    boost: 2
---

#   Execute Command

[**Item Action Type**][1]

Executes a command with the entity holding the item stack as the source. (e.g: `@s` will select the entity itself)

Type ID: `eggolib:execute_command`


Fields | Type | Default | Description
-------|------|---------|------------
`command` | [**String**][2] | | The command to execute.


### Examples

=== "Example #1"

    ```json
    "item_action": {
        "type": "eggolib:execute_command",
        "command": "say Hello world!"
    }
    ```

    This example will execute the `/say Hello world!` command as the entity that is holding the item stack.



[1]: ../item_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
