---
title: Prevent Critical Hit (Power Type)
date: 2023-01-31
search:
    boost: 2
---

#   Prevent Critical Hit

[**Power Type**][1]

Prevents the player from dealing critical hits.

Type ID: `eggolib:prevent_critical_hit`


!!! note

    In the context of this power type, the 'actor' will be the entity that dealt the critical hit whilst the 'target' will be the entity that was hit.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [**Bi-entity Action Type**][2] | *optional* | If specified, this action will be executed on either or both the 'actor' and 'target' upon the power preventing critical hits.
`bientity_condition` | [**Bi-entity Condition Type**][3] | *optional* | If specified, the power will only prevent critical hits if this condition is fulfilled by either or both the 'actor' and the 'target'.
`damage_condition` | [**Damage Condition Type**][4] | *optional* | If specified, the power will only prevent critical hits if this condition is fulfilled by the damage dealt by the 'actor'.
`priority` | [**Integer**][5] | `0` | Determines the priority of the power. Powers with higher priority value will be triggered first.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:prevent_critical_hit",
        "bientity_action": {
            "type": "apoli:actor_action",
            "action": {
                "type": "apoli:execute_command",
                "command": "title @s actionbar {\"text\": \"Cannot deal critical hits!\", \"color\": \"red\"}"
            }
        }
    }
    ```

    This example will prevent the player from dealing critical hits.


=== "Example #2"

    ``` json
    {
        "type": "eggolib:prevent_critical_hit",
        "bientity_condition": {
            "type": "apoli:target_condition",
            "condition": {
                "type": "eggolib:has_tag",
                "tag": "excluded"
            },
            "inverted": true
        }
    }
    ```

    This example will prevent the player from dealing critical hits to entities that have the `excluded` tag added via the `/tag` command



[1]: ../power_types.md
[2]: ../bientity_action_types.md
[3]: ../bientity_condition_types.md
[4]: ../damage_condition_types.md
[5]: https://origins.readthedocs.io/en/latest/types/data_types/integer
