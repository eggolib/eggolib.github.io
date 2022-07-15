---
title: Set Perspective (Entity Action Types)
date: 2022-07-14
search:
    boost: 1
---

#   Set Perspective

**[Entity Action Type]**

Sets the perspective of the player.

Type ID: `eggolib:set_perspective`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`perspective` | **[Perspective]** | | The perspective to use.


### Examples

``` json
"entity_action": {
    "type": "eggolib:set_perspective",
    "perspective": "first_person"
}
```

This example will set the perspective of the player to first person.



[Entity Action Type]: ../entity_action_types.md
[Perspective]: ../data_types/perspective.md
