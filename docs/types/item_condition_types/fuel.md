---
title: Fuel (Item Condition Type)
date: 2023-06-18
search:
    boost: 2
---

#   Fuel

[**Item Condition Type**][1]

Checks whether the item stack is considered as fuel.

Type ID: `eggolib:fuel`


!!! note

    If the `comparison` or `compare_to` fields are not present, this item condition type will check if the item stack is considered as fuel.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | *optional* | Determines how to compare the fuel time of the item stack to the specified value.
`compare_to` | [**Integer**][3] | *optional* | The value to compare the fuel time of the item stack to.


### Examples

=== "Example #1"

    ```json
    "item_condition": {
        "type": "eggolib:fuel"
    }
    ```

    This example will check if the item stack is considered as fuel.


=== "Example #2"

    ```json
    "item_condition": {
        "type": "eggolib:fuel",
        "comparison": ">=",
        "compare_to": 100
    }
    ```

    This example will check if the item stack is considered as fuel and if its fuel time is equal or greater than 100.



[1]: ../item_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
