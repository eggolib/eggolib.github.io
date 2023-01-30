---
title: Clear Key Cache (Entity Action Type)
date: 2022-08-24
search:
    boost: 2
---

#   Clear Key Cache

[**Entity Action Type**][1]

Clears the key sequence cache of a power that uses the [**Action on Key Sequence (Power Type)**][2].

Type ID: `eggolib:clear_key_cache`


!!! danger

    This entity action type has been **deprecated** and will be removed in a future version. Please use [**Modify Key Sequence (Entity Action Type)**][3] instead.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [**Identifier**][4] | | The namespace and ID of the power to clear the key sequence cache of.


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:clear_key_cache",
        "power": "example:power"
    }
    ```

    This example will clear the key sequence cache of the `example:power` *(`data/example/powers/power.json`)* power.



[1]: ../entity_action_types.md
[2]: ../power_types/action_on_key_sequence.md
[3]: modify_key_sequence.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/identifier