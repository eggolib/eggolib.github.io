---
title: Has Tag (Entity Condition Type)
date: 2022-07-27
search:
    boost: 1
---

#   Has Tag

**[Entity Condition Type]**

Checks if the entity has a scoreboard tag *(added via the `/tag` command).*

Type ID: `eggolib:has_tag`


!!! note

    If neither the `tag` or `tags` fields are specified, this entity condition type will check if the entity has any scoreboard tags.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`tag`  | **[String]** | *optional* | If specified, checks if the entity has this scoreboard tag.
`tags` | **[Array]** of **[Strings]** | *optional* | If specified, checks if the entity has these scoreboard tags.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:has_tag",
        "tag": "example.tag"
    }
    ```

    This example will check if the entity has the `example.tag` scoreboard tag.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:has_tag",
        "tags": [
            "tag_with_numbers123",
            "tagWithUppercasedLetters"
        ]
    }
    ```

    This example will check if the entity has the `tag_with_numbers123` or the `tagWithUppercasedLetters` scoreboard tags.



[Entity Condition Type]: ../entity_condition_types.md
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
[Array]: https://origins.readthedocs.io/en/latest/types/data_types/array
[Strings]: https://origins.readthedocs.io/en/latest/types/data_types/string
