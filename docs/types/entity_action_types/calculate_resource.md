---
title: Calculate Resource (Entity Action Type)
date: 2022-07-14
search:
    boost: 2
---

#   Calculate Resource

**[Entity Action Type]**

Calculates the value of a power that uses the **[Resource (Power Type)]** from the value of another power that uses the **[Resource (Power Type)]**.

Type ID: `eggolib:calculate_resource`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`target` | **[Identifier]** | | The namespace, path and ID of the power to calculate the value of.
`operation` | **[Math Operation]** | `"add"` | Determines how the value of the source power will be calculated to the value of the target power.
`source` | **[Identifier]** | | The namespace, path and ID of the power to use the value of.


### Examples

``` json
"entity_action": {
    "type": "eggolib:calculate_resource",
    "target": "example:resource_a",
    "operation": "multiply",
    "source": "example:resource_b"
}
```

This example will multiply the value of the `example:resource_a` *(`data/example/powers/resource_a.json`)* power by the value of the `example:resource_b` *(`data/example/powers/resource_b.json`)* power.



[Entity Action Type]: ../entity_action_types.md
[Resource (Power Type)]: https://origins.readthedocs.io/en/latest/types/power_types/resource
[Identifier]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[Math Operation]: ../data_types/math_operation.md
