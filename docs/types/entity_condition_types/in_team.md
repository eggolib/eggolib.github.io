---
title: In Team (Entity Condition Type)
date: 2023-01-30
search:
    boost: 2
---

#   In Team

[**Entity Condition Type**][1]

Checks if the entity is in the specified team(s).

Type ID: `eggolib:in_team`


!!! note

    If neither the `team` or `teams` field is present, this entity condition type will check if the entity is in any team.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`team` | [**Abstract Team**][2] | *optional* | If specified, check if the entity is in this team.
`teams` | [**Array**][3] of [**Abstract Teams**][2] | *optional* | If specified, check if the entity is in any of these teams.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:in_team"
    }
    ```

    This example will check if the entity is in any team.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:in_team",
        "team": {
            "name": "epicGamers"
        }
    }
    ```

    This example will check if the entity is in a team with the name "epicGamers".


=== "Example #3"

    ``` json
    "condition": {
        "type": "eggolib:in_team",
        "teams": [
            {
                "name": "epicGamers"
            },
            {
                "nametag_visibility": "never"
            }
        ]
    }
    ```

    This example will check if the entity is in a team with the name "epicGamers" or a team that has the `nametagVisibility` option set to `never`.



[1]: ../entity_condition_types.md
[2]: ../data_types/abstract_team.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
