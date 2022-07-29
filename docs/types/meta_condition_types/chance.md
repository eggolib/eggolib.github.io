---
title: Chance (Meta Condition Type)
date: 2022-07-29
search:
    boost: 2
---

#   Chance

**[Meta Condition Type]**

Generates a random value ranging from 0.0 to 1.0 and checks if it's less than the specified value.

Type ID: `eggolib:chance`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`chance` | **[Float]** | | The value to compare the generated random value to.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:chance",
        "chance": 0.5
    }
    ```

    This example will evaluate to true 50% of the time.



[Meta Condition Type]: ../meta_condition_types.md
[Float]: https://origins.readthedocs.io/en/latest/types/data_types/float
