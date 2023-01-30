---
title: Height (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Height

[**Dimension Type Condition Type**][1]

Compares the maximum height in which blocks can exist of the dimension to the specified value.

Type ID: `eggolib:height`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the maximum height in which blocks can exist of the dimension is compared to the specified value.
`compare_to` | [**Integer**][3] | | The value which the maximum height in which blocks can exist of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:height",
        "comparison": "==",
        "compare_to": 384
    }
    ```

    This example will check if the maximum height of the dimension is 384. For instance, the Overworld dimension fulfills this condition.


=== "Example #2"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:height",
        "comparison": "<=",
        "compare_to": 256
    }
    ```

    This example will check if the maximum height of the dimension is equal to or less than 256. For instance, The Nether dimension fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
