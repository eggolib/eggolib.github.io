---
title: Perspective (Entity Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   Perspective

[**Entity Condition Type**][1]

Checks the current perspective of the player.

Type ID: `eggolib:perspective`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`perspective` | [**Perspective**][2] | *optional* | If specified, the condition will evaluate to true if the player has this set as their perspective.
`perspectives` | [**Array**][3] of [**Perspectives**][2] | *optional* | If specified, the condition will evaluate to true if the player has one of these set as their perspective.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:perspective",
        "perspective": "first_person"
    }
    ```

    This example will check if the player is in first person perspective.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:perspective",
        "perspectives": [
            "third_person_back",
            "third_person_front"
        ]
    }
    ```

    This example will check if the player is in either third person (back) or third person (front) perspectives.



[1]: ../entity_condition_types.md
[2]: ../data_types/perspective.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
