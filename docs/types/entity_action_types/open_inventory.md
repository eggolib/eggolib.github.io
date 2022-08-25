---
title: Open Inventory (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Open Inventory

**[Entity Action Type]**

Opens an inventory.

Type ID: `eggolib:open_inventory`

!!! caution

    Currently, this entity action type does not open the inventory of the player that invoked the action.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | **[Identifier]** | *optional* | If specified, the inventory of this power will be opened instead.


### Examples

``` json
"entity_action": {
    "type": "eggolib:open_inventory",
    "power": "example:extra_inventory"
}
```

This example will open the inventory of the `example:extra_inventory` *(`data/example/powers/extra_inventory.json`)* as long as that power uses the `inventory` power type.


[Entity Action Type]: ../entity_action_types.md
[Identifier]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
