---
title: Min Y (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Min Y

[**Dimension Type Condition Type**][1]

Compares the minimum height in which blocks can exist of the dimension to the specified value.

Type ID: `eggolib:min_y`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the minimum height of the dimension is compared to the specified value.
`compare_to` | [**Integer**][3] | | The value which the minimum height of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:min_y",
        "comparison": "<",
        "compare_to": 0
    }
    ```

    This example will check if the minimum height of the dimension is less than 0. For instance, the Overworld dimension fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
