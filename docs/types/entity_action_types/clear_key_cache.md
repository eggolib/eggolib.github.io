---
title: Clear Key Cache (Entity Action Type)
date: 2022-08-24
search:
    boost: 2
---

#   Clear Key Cache

**[Entity Action Type]**

Clears the key sequence cache of a power that uses the Action on Key Sequence power type.

Type ID: `eggolib:clear_key_cache`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | **[Identifier]** | | The namespace and ID of the power to clear the key sequence cache of.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:clear_key_cache",
        "power": "example:power"
    }
    ```

    This example will clear the key sequence cache of the `example:power` *(`data/example/powers/power.json`)* power.



[Entity Action Type]: ../entity_action_types.md
[Identifier]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
