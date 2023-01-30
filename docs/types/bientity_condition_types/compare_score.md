---
title: Compare Score (Bi-entity Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   Compare Score

[**Bi-entity Condition Type**][1]

Compares the score of the actor from a scoreboard objective to the score of the target from another scoreboard objective.

Type ID: `eggolib:compare_score`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`actor_objective` | [**String**][2] | | The name of the scoreboard objective that stores the score of the actor.
`target_objective` | [**String**][2] | | The name of the scoreboard objective that stores the score of the target.
`comparison` | [**Comparison**][3] | `"=="` | Determines how the scores of the actor and target are compared.


### Examples

=== "Example #1"

    ``` json
    "bientity_condition": {
        "type": "eggolib:compare_score",
        "actor_objective": "a.id",
        "target_objective": "t.id",
        "comparison": "=="
    }
    ```

    This example will check if the score of the actor in the `a.id` scoreboard objective is equal to the score of the target in the `t.id` scoreboard objective.



[1]: ../bientity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
[3]: https://origins.readthedocs.io/en/latest/types/data_types/comparison
