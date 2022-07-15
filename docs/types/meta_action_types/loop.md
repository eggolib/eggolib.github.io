---
title: Loop (Meta Action Types)
date: 2022-07-14
search:
    boost: 1
---

#   Loop

**[Meta Action Type]**

Executes an action for the specified amount of iterations.

Type ID: `eggolib:loop`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`before_action` | **[Action Type]** | *optional* | If specified, this action will be executed before the loop starts.
`action` | **[Action Type]** | *optional* | If specified, this action will be executed for each iteration of the loop.
`after_action` | **[Action Type]** | *optional* | If specified, this action will be executed after the loop ends.
`score` | **[Scoreboard]** | *optional* | If specified, this value will be used as the amount of iterations for the loop.
`value` | **[Integer]** | *optional* | If specified and if `score` is not specified, this value will be used as the amount of iterations for the loop.


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



[Meta Action Type]: ../meta_action_types.md
[Action Type]: https://origins.readthedocs.io/en/1.4.1/types/action_types
[Scoreboard]: ../data_types/scoreboard.md
[Integer]: https://origins.readthedocs.io/en/1.4.1/types/data_types/integer