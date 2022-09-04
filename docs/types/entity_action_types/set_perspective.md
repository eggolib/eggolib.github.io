---
title: Set Perspective (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Set Perspective

[**Entity Action Type**][1]

Sets the perspective of the player.

Type ID: `eggolib:set_perspective`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`perspective` | [**Perspective**][2] | | The perspective to use.


### Examples

``` json
"entity_action": {
    "type": "eggolib:set_perspective",
    "perspective": "first_person"
}
```

This example will set the perspective of the player to first person.



[1]: ../entity_action_types.md
[2]: ../data_types/perspective.md
