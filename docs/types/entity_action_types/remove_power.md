---
title: Remove Power (Entity Action Types)
date: 2022-07-14
search:
    boost: 1
---

#   Remove Power

**[Entity Action Type]**

Removes a power from the entity.

Type ID: `eggolib:remove_power`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | **[Identifier]** | | The namespace, path and ID of the power to be removed.


### Examples

``` json
"entity_action": {
    "type": "eggolib:remove_power",
    "power": "example:phasing"
}
```

This example will remove the `example:phasing` *(`data/example/powers/phasing.json`)* power from the entity that invoked the action.



[Entity Action Type]: ../entity_action_types.md
[Identifier]: https://origins.readthedocs.io/en/1.4.1/types/data_types/identifier
