---
title: Scoreboard (Entity Condition Type)
date: 2022-07-14
search:
    boost: 2
---

#   Scoreboard

[**Entity Condition Type**][1]

Compares the score of the entity *(or score holder)* from a specified scoreboard objective to the specified value.

!!! note

    If the entity or score holder does not have a score from the specified scoreboard objective, this condition would return false even if the `"!="` comparison is used. You can use the `"!="` comparison in combination with the `"=="` comparison to test if the entity or score holder does not have a score in the specified scoreboard objective.

!!! caution

    This condition is only effective server-side, meaning that using the condition in client-sided power types will not work properly.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`name` | [**String**][2] | *optional* | If specified, the condition will check for the score of this score holder instead of the entity.
`objective` | [**String**][2] | | The name of the scoreobard objective to retrieve the score of the entity or score holder from.
`comparison` | [**Comparison**][3] | | Determines how the score of the entity or score holder should be compared to the specified value.
`compare_to` | [**Integer**][4] | | The value which the score of the entity or score holder should be compared to.


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



[1]: ../entity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
[3]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
[4]: https://origins.readthedocs.io/en/latest/types/data_types/integer
