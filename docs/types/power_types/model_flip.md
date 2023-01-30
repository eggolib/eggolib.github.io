---
title: Model Flip (Power Type)
date: 2022-07-27
search:
    boost: 2
---

#   Model Flip

[**Power Type**][1]

Flips the model of the entity, similar to how Dinnerbone's model is flipped.

Type ID: `eggolib:model_flip`


### Fields

*None.*


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:model_flip"
    }
    ```

    This example will flip the model of the entity that has the power.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:model_flip",
        "condition": {
            "type": "apoli:sneaking"
        }
    }
    ```

    This example will flip the model of the entity that has the power if the entity is sneaking.



[1]: ../power_types.md