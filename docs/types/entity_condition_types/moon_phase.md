---
title: Moon Phase (Entity Condition Type)
date: 2023-03-11
search:
    boost: 2
---

#   Moon Phase

[**Entity Condition Type**][1]

Checks the current moon phase of the world.

Type ID: eggolib:moon_phase


### Fields

Field | Type | Default | Description
------|------|---------|------------
`phase` | [**Moon Phase**][2] | *optional* | If specified, checks if the current moon phase of the world matches this moon phase.
`phases` | [**Array**][3] of [**Moon Phases**][2] | *optional* | If specified, checks if the current moon phase of the world matches any of these moon phases.


### Examples

=== "Example #1"

    ```json
    "condition": {
        "type": "eggolib:moon_phase",
        "phase": "full_moon"
    }
    ```

    This example will check if the current moon phase of the world is Full Moon.


=== "Example #2"

    ```json
    "condition": {
        "type": "eggolib:moon_phase",
        "phases": [
            "full_moon",
            "new_moon"
        ]
    }
    ```

    This example will check if the current moon phase of the world is either Full Moon or New Moon.



[1]: ../entity_condition_types.md
[2]: ../data_types/moon_phase.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
