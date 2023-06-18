---
title: Colliding (Bi-entity Condition Type)
date: 2023-06-18
search:
    boost: 2
---

#   Colliding

[**Bi-entity Condition Type**][1]

Checks if the actor entity is colliding with the target entity.

Type ID: eggolib:colliding


### Fields

Field | Type | Default | Description
------|------|---------|------------
`offset` | [**Vector**][2] | *optional* | If specified, this offset will be applied to the actor entity's bounding box.


### Examples

=== "Example #1"

    ```json
    "bientity_condition": {
        "type": "eggolib:colliding"
    }
    ```


=== "Example #2"

    ```json
    "bientity_condition": {
        "type": "apoli:or",
        "conditions": [
            {
                "type": "eggolib:colliding",
                "offset": {
                    "x": 0.5,
                    "y": 0.0,
                    "z": 0.5
                }
            },
            {
                "type": "eggolib:colliding",
                "offset": {
                    "x": -0.5,
                    "y": 0.0,
                    "z": -0.5
                }
            }
        ]
    }
    ```



[1]: ../bientity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/vector
