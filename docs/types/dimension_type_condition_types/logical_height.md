---
title: Logical Height (Dimension Type Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Logical Height

[**Dimension Type Condition Type**][1]

Compares the maximum logical height *(for Nether portals and Chorus Fruits)* of the dimension to the specified value.

Type ID: `eggolib:logical_height`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`comparison` | [**Comparison**][2] | | Determines how the maximum logical height of the dimension is compared to the value.
`compare_to` | [**Integer**][3] | | The value which the maximum logical height of the dimension is compared to.


### Examples

=== "Example #1"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:logical_height",
        "comparison": "==",
        "compare_to": 384
    }
    ```

    This example will check if the maximum logical height of the dimension is 384. For instance, the Overworld dimension fulfills this condition.


=== "Example #2"

    ``` json
    "dimension_type_condition": {
        "type": "eggolib:logical_height",
        "comparison": "<=",
        "compare_to": 256
    }
    ```

    This example will check if the maximum logical height of the dimension is 384 or less. For instance, The Nether dimension fulfills this condition.



[1]: ../dimension_type_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[3]: https://origins.readthedocs.io/en/latest/types/data_types/integer
