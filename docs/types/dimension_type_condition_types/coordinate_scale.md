---
title: Coordinate Scale (Dimension Type Condition Type)
date: 2022-01-30
search:
    boost: 2
---

#   Coordinate Scale

[**Dimension Type Condition Type**][1]

Compares the value used for scaling the coordinates of an entity when entering/leaving the dimension to the specified value.

Type ID: `eggolib:coordinate_scale`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the coordinate scale property of the dimension is compared to the specified value.
`compare_to` | [**Float**][3] | | The value which the coordinate scale property of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:coordinate_scale",
        "comparison": "==",
        "compare_to": 1
    }
    ```

    This example will check if the scaling coordinate value of the dimension is 1. For instance, the Overworld and The End dimensions will fulfill this condition.


=== "Example #2"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:coordinate_scale",
        "comparison": ">=",
        "compare_to": 8
    }
    ```

    This example will check if the scaling coordinate value of the dimension is 8. For instance, The Nether fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/float
