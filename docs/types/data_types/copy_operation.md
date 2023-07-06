---
title: Copy Operation (Data Type)
date: 2023-07-06
search:
    boost: 2
---

#   Copy Operation

[**Data Type**][1]

An [**object**][2] that determines how NBT is copied from the specified source NBT path to the target NBT path.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`source` | [**NBT Path**][3] | | The NBT path to copy from.
`target` | [**NBT Path**][3] | | The NBT path to copy to.
`op` | [**String**][4] | | Determines how the NBT is copied. Accepts either `"replace"`, `"merge"` (for merging objects) or `"append"` (for adding to the end of an array).


### Examples

=== "Example #1"

    ```json
    "ops": [
        {
            "source": "Item.tag.gems",
            "target": "collectedGems",
            "op": "replace"
        }
    ]
    ```

    This example will completely replace the contents of the `collectedGems` NBT path with the data from the `Item.tag.gems` NBT path.


=== "Example #2"

    ```json
    "ops": [
        {
            "source": "Item.tag",
            "target": "tag",
            "op": "merge"
        }
    ]
    ```

    This example will merge the contents of the `Item.tag` NBT path to the `tag` NBT path, meaning that new NBTs will be added and NBTs that exist in both the target and source paths are replaced by the NBT from the source.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/object
[3]: ../data_types/nbt_path.md
[4]: https://origins.readthedocs.io/en/latest/types/data_types/string
