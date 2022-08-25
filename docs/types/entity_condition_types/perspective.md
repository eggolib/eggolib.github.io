---
title: Perspective (Entity Condition Types)
date: 2022-07-14
search:
    boost: 2
---

#   Perspective

**[Entity Condition Type]**

Checks the current perspective of the player.

Type ID: `eggolib:perspective`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`perspective` | **[Perspective]** | *optional* | If specified, the condition will evaluate to true if the player has this set as their perspective.
`perspectives` | **[Array]** of **[Perspectives]** | *optional* | If specified, the condition will evaluate to true if the player has one of these set as their perspective.


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



[Entity Condition Type]: ../entity_condition_types.md
[Perspective]: ../data_types/perspective.md
[Perspectives]: ../data_types/perspective.md
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
