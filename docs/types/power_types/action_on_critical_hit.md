---
title: Action on Critical Hit (Power Type)
date: 2023-01-31
search:
    boost: 2
---

#   Action on Critical Hit

[**Power Type**][1]

Executes an action upon dealing a critical hit.

Type ID: `eggolib:action_on_critical_hit`


!!! note

    In the context of this power type, the 'actor' will be the entity that dealt the critical hit while the 'target' will be the entity that was hit.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`bientity_action` | [**Bi-entity Action Type**][2] | *optional* | If specified, this action will be executed on either or both the 'actor' and the 'target' upon the 'actor' dealing a critical hit.
`bientity_condition` | [**Bi-entity Condition Type**][3] | *optional* | If specified, the action will only be executed if this condition is fulfilled by either or both the 'actor' and the 'target'.
`damage_condition` | [**Damage Condition**][4] | *optional* | If specified, the action will only be executed if this condition is fulfilled by the damage dealt by the 'actor'.
`priority` | [**Integer**][5] | `0` | Determines the priority of the power. Powers will higher priority value will be triggered first.


### Examples

=== "Example #1"

    ``` json
    {
        "type": "eggolib:action_on_critical_hit",
        "bientity_action": {
            "type": "apoli:target_action",
            "action": {
                "type": "apoli:execute_command",
                "command": "say Ouch!!!"
            }
        }
    }
    ```

    This example will execute a `/say Ouch!!!` command as the 'target' upon the 'actor' dealing a critical hit on the 'target'.




[1]: ../power_types.md
[2]: ../bientity_action_types.md
[3]: ../bientity_condition_types.md
[4]: ../damage_condition_types.md
[5]: https://origins.readthedocs.io/en/latest/types/data_types/integer
