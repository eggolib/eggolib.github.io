---
title: Loop (Meta Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Loop

[**Meta Action Type**][1]

Executes an action for the specified amount of iterations.

Type ID: `eggolib:loop`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`before_action` | [**Action Type**][2] | *optional* | If specified, this action will be executed before the loop starts.
`action` | [**Action Type**][2] | *optional* | If specified, this action will be executed for each iteration of the loop.
`after_action` | [**Action Type**][2] | *optional* | If specified, this action will be executed after the loop ends.
`score` | [**Scoreboard**][3] | *optional* | If specified, this value will be used as the amount of iterations for the loop.
`value` | [**Integer**][4] | *optional* | If specified and if `score` is not specified, this value will be used as the amount of iterations for the loop.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:loop",
        "action": {
            "type": "apoli:execute_command",
            "command": "say Hello!"
        },
        "value": 3
    }
    ```

    This example will make the entity that invoked the action say "Hello!" thrice.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:loop",
        "action": {
            "type": "apoli:heal",
            "amount": 2
        },
        "score": {
            "name": "amountOfHeals",
            "objective": "example"
        }
    }
    ```

    This example will heal the entity that invoked the action depending on the score of the `amountOfHeals` score holder in the `example` scoreboard objective. If it doesn't exist, the action will simply do nothing.



[1]: ../meta_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/action_types
[3]: ../data_types/scoreboard.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/integer
