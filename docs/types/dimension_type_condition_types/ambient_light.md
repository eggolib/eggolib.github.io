---
title: Ambient Light (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Ambient Light

[**Dimension Type Condition Type**][1]

Compares the ambient light property of the dimension to the specified value.

Type ID: `eggolib:ambient_light`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the ambient light property of the dimension is compared to the specified value.
`compare_to` | [**Float**][3] | | The value which the ambient light property of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:ambient_light",
        "comparison": "==",
        "compare_to": 0.0
    }
    ```

    This example will check if the dimension has no ambient light. For instance, the Overworld and The End dimensions fulfill this condition.


=== "Example #2"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:ambient_light",
        "comparison": ">=",
        "compare_to": 0.1
    }
    ```

    This example will check if the dimension has an ambient light of 0.1 or higher. For instance, The Nether dimension fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/float
