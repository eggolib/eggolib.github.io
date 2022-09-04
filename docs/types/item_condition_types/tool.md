---
title: Tool (Item Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   Tool

[**Item Condition Type**][1]

Checks whether the item is a tool or if it's an instance of a certain tool type.

Type ID: `eggolib:tool`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`tool_type` | [**String**][2] | *optional* | If specified, the condition will evaluate to true if the item is an instance of this tool type. Accepts one of `"axe"`, `"hoe"`, `"pickaxe"`, `"shovel"`, `"sword"` and `"shears"`.
`tool_types` | [**Array**][3] of [**Strings**][2] | *optional* | If specified, the condition will evaluate to true if the item is an instance of one of these tool types. Accepts `"axe"`, `"hoe"`, `"pickaxe"`, `"shovel"`, `"sword"` and `"shears"`.


### Examples

=== "Example #1"

    ``` json
    "item_condition": {
        "type": "eggolib:tool",
        "tool_type": "sword"
    }
    ```

    This example will check if the item is a Sword.


=== "Example #2"

    ``` json
    "item_condition": {
        "type": "eggolib:tool",
        "tool_types": [
            "axe",
            "pickaxe"
        ]
    }
    ```

    This example will check if the item is either an Axe or a Pickaxe.



[1]: ../item_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
