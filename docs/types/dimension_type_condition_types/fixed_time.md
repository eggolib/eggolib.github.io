---
title: Fixed Time (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Fixed Time

[**Dimension Type Condition Type**][1]

Compares the fixed time property of the dimension to the specified value.

Type ID: `eggolib:fixed_time`


!!! note

    If neither the `comparison` and `compare_to` is present, this dimension type condition type will check if the dimension has a fixed time.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | *optional* | Determines how the fixed time property of the dimension is compared to the specified value.
`compare_to` | [**Integer**][3] | *optional* | The value which the fixed time property of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:fixed_time"
    }
    ```

    This example will check if the dimension has a fixed time.


=== "Example #2"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:fixed_time",
        "comparison": "==",
        "compare_to": 18000
    }
    ```

    This example will check if the dimension has its time fixed at midnight.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
