---
title: Scoreboard (Entity Condition Types)
date: 2022-07-14
search:
    boost: 2
---

#   Scoreboard

**[Entity Condition Type]**

Compares the score of the entity *(or score holder)* from a specified scoreboard objective to the specified value.

!!! note

    If the entity or score holder does not have a score from the specified scoreboard objective, this condition would return false even if the `"!="` comparison is used. You can use the `"!="` comparison in combination with the `"=="` comparison to test if the entity or score holder does not have a score in the specified scoreboard objective.

!!! caution

    This condition is only effective server-side, meaning that using the condition in client-sided power types will not work properly.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`name` | **[String]** | *optional* | If specified, the condition will check for the score of this score holder instead of the entity.
`objective` | **[String]** | | The name of the scoreobard objective to retrieve the score of the entity or score holder from.
`comparison` | **[Comparison]** | | Determines how the score of the entity or score holder should be compared to the specified value.
`compare_to` | **[Integer]** | | The value which the score of the entity or score holder should be compared to.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:scoreboard",
        "objective": "example",
        "comparison": ">=",
        "compare_to": 1
    }
    ```

    This example will check if the entity has a score of 1 or greater in the `example` scoreboard objective.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:scoreboard",
        "name": "testScoreHolder",
        "objective": "example",
        "comparison": "==",
        "compare_to": 10
    }
    ```

    This example will check if the `testScoreHolder` score holder from the `example` scoreboard objective has a score of 10.



[Entity Condition Type]: ../entity_condition_types.md
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Comparison]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[Integer]: https://origins.readthedocs.io/en/latest/types/data_types/integer
