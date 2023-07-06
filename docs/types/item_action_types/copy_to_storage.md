---
title: Copy to Storage (Item Action Type)
date: 2023-07-06
search: 
    boost: 2
---

#   Copy to Storage

[**Item Action Type**][1]

Copies the data of the item stack to a command NBT storage.

Type ID: `eggolib:copy_to_storage`


!!! note

    The data of the item stack, such as its ID (`id`), count (`Count`), and NBTs (`tag`), are stored in an object named `Item`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`id` | [**Identifier**][2] | | The identifier of the command NBT storage to put the data of the item stack to.
`ops` | [**Array**][3] of [**Copy Operations**][4] | | The operations to use to copy NBT from the item stack to the specified command NBT storage.


### Examples

=== "Example #1"

    ```json
    "item_action": {
        "type": "eggolib:copy_to_storage",
        "id": "example:storage",
        "ops": [
            {
                "source": "Item",
                "target": "collectedItems",
                "op": "append"
            }
        ]
    }
    ```

    This example will copy and add the object that contains the ID, count, and NBTs of the item stack to the `collectedItems` array NBT path of the `example:storage` command NBT storage.


=== "Example #2"

    ```json
    "item_action": {
        "type": "eggolib:copy_to_storage",
        "id": "example:storage",
        "ops": [
            {
                "source": "Item.Count",
                "target": "amountOfItems",
                "op": "replace"
            }
        ]
    }
    ```

    This example will replace the value of the `amountOfItems` NBT path of the `example:storage` command NBT storage with the count value of the item stack.



[1]: ../item_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/identifier
[3]: https://origins.readthedocs.io/en/latest/types/data_types/array
[4]: ../data_types/copy_operation.md
