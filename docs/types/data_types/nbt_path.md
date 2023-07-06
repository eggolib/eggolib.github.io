---
title: NBT Path (Data Type)
date: 2023-07-06
search:
    boost: 2
---

#   NBT Path

[**Data Type**][1]

A [**string**][2] that specifies a collection of elements from an NBT.


!!! note

    See [**Minecraft Fandom Wiki: NBT path format**][3] for more information about NBT paths.


### Examples

=== "Example #1"

    ```json
    "source": "VillagerData"
    ```

    This example will specify the `VillagerData` NBT.


=== "Example #2"

    ```json
    "source": "Items[0].tag"
    ```

    This example will specify the `tag` NBT from the first element (index of 0) of the `Items[]` array NBT.


=== "Example #3"

    ```json
    "source": "Item.tag.gems[-1]"
    ```

    This example will specify the last element from the `gems` array NBT of the `tag` object NBT from the `Item` object NBT.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
[3]: https://minecraft.fandom.com/wiki/NBT_path_format
