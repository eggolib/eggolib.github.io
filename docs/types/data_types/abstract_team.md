---
title: Abstract Team (Data Type)
date: 2023-01-30
search:
    boost: 2
---

#   Abstract Team

[**Data Type**][1]

An [**object**][2] used for abstractly representing a team.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`name` | [**String**][3] | *optional* | The name of the team.
`friendly_fire` | [**Boolean**][4] | *optional* | Determines whether the team should allow friendly fire or not.
`show_friendly_invisibles` | [**Boolean**][4] | *optional* | Determines whether the team should show teammates that are invisible.
`nametag_visibility` | [**Visibility Rule**][5] | *optional* | Determines the visibility for the nametag of the entities within the team.
`death_message_visibility` | [**Visibility Rule**][5] | *optional* | Determines the visibility for the death message of the entities within the team.
`collision_rule` | [**Collision Rule**][6] | *optional* | Determines how entity collision behaves for the entities within the team.


### Examples

=== "Example #1"
    
    ``` json
    "team": {
        "name": "epicGamers"
    }
    ```

    This example abstractly represents a team with the name "epicGamers".


=== "Example #2"

    ``` json
    "team": {
        "nametag_visibility": "never"
    }
    ```

    This example abstractly represents a team with the `nametagVisibility` option set to `never`.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/object
[3]: https://origins.readthedocs.io/en/latest/types/data_types/string
[4]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
[5]: visibility_rule.md
[6]: collision_rule.md
