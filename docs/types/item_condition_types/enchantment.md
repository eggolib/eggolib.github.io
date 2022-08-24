---
title: Enchantment
date: 2022-08-24
search:
    boost: 2
---

#   Enchantment

**[Item Condition Type]**

Checks whether the item is enchanted.

Type ID: `eggolib:enchantment`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`enchantment` | **[Identifier]** | *optional* | If specified, the condition will check if the item has this specific enchantment.
`comparison` | **[Comparison]** | `">="` | Determines how the level of the specified enchantment is compared to the specified value. If `enchantment` is not present, this will determine how the count of available enchantments in the item is compared to the specified value instead.
`compare_to` | **[Integer]** | `1` | The specified value to compare the level of the specified enchantment to. If `enchantment` is not present, this will be compared to the count of available enchantments in the item instead.


### Examples

=== "Example #1"

    ``` json
    "item_condition": {
        "type": "eggolib:enchantment",
        "comparison": ">=",
        "compare_to": 1
    }
    ```

    This example will check if the item has one or more enchantments.


=== "Example #2"

    ``` json
    "item_condition": {
        "type": "eggolib:enchantment",
        "enchantment": "minecraft:mending",
        "comparison": "==",
        "compare_to": 1
    }
    ```

    This example will check if the item has the Mending I enchantment.



[Item Condition Type]
[Identifier]
[Comparison]
[Integer]
