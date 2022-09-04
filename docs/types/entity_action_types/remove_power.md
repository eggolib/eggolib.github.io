---
title: Remove Power (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Remove Power

[**Entity Action Type**][1]

Removes a power from the entity.

Type ID: `eggolib:remove_power`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [**Identifier**][2] | | The namespace, path and ID of the power to be removed.


### Examples

``` json
"entity_action": {
    "type": "eggolib:remove_power",
    "power": "example:phasing"
}
```

This example will remove the `example:phasing` *(`data/example/powers/phasing.json`)* power from the entity that invoked the action.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
