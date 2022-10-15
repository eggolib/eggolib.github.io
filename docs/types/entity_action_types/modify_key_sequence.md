---
title: Modify Key Sequence (Entity Action Type)
date: 2022-10-15
search:
    boost: 2
---

#   Modify Key Sequence

[**Entity Action Type**][1]

Modifies the current key sequence of a power that uses the [**Action on Key Sequence (Power Type)**][2] present on the entity that invoked the action.

Type ID: `eggolib:modify_key_sequence`


!!! note

    If `index` is less than or equal to `-1`, then it would refer to the last index of the current key sequence. Otherwise, if it's `0`, then it would refer to the first index of the current key sequence.


!!! note

    Here's an explanation on how each operation works:

    * `"append"`  - Adds the specified keys to the last index of the current key sequence.
    * `"insert"`  - Inserts the specified keys to the specified index of the current key sequence.
    * `"prepend"` - Adds the specified keys to the first index of the current key sequence.
    * `"remove"`  - Removes the specified keys from the current key sequence. If there are no keys specified, remove the key from the specified index instead.
    * `"set"`     - Replace the current key sequence with the specified key sequence.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`power` | [**Identifier**][3] | | The namespace and ID of the power to modify its current key sequence of.
`operation` | [**String**][4] | `"append"` | Determines how the specified keys are operated on the current key sequence of the specified power. Accepts `"append"`, `"insert"`, `"prepend"`, `"remove"` or `"set"`.
`keys` | [**Array**][5] of [**Keys**][6] | *optional* | If specified, these keys will be used to modify the current key sequence of the specified power.
`index` | [**Integer**][7] | `-1` | The integer to use as the index when modifying the current key sequence of the specified power. **Only used by the `"insert"` and `"remove"` operations.**


### Examples

=== "Example #1"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_key_sequence",
        "power": "example:power",
        "operation": "set",
        "keys": []
    }
    ```

    This example will essentially clear the current key sequence of the `example:power` power.


=== "Example #2"

    ``` json
    "entity_action": {
        "type": "eggolib:modify_key_sequence",
        "power": "example:power",
        "operation": "remove"
    }
    ```

    This example will remove the key from the last index of the current key sequence of the `example:power` power.



[1]: ../entity_action_types.md
[2]: ../power_types/action_on_key_sequence.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[4]: https://origins.readthedocs.io/en/latest/types/data_types/string
[5]: https://origins.readthedocs.io/en/latest/types/data_types/array
[6]: ../data_types/key.md
[7]: https://origins.readthedocs.io/en/latest/types/data_types/integer
