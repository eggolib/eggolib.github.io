---
title: Open Inventory (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Open Inventory

[**Entity Action Type**][1]

Opens an inventory.

Type ID: `eggolib:open_inventory`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [**Identifier**][2] | *optional* | If specified, the inventory of this power will be opened instead.


### Examples

``` json
"entity_action": {
    "type": "eggolib:open_inventory",
    "power": "example:extra_inventory"
}
```

This example will open the inventory of the `example:extra_inventory` *(`data/example/powers/extra_inventory.json`)* as long as that power uses the `inventory` power type.



[1]: ../entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
