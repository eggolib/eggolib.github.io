---
title: Scoreboard (Data Type)
date: 2022-07-14
search:
    boost: 1
---

#   Scoreboard

**[Data Type]**

An object used for getting the score of a score holder from a scoreboard objective.

!!! note

    If the score holder referenced in the `name` field does not exist, the data type will return a value of 0.

!!! caution

    The `name` field of the data type does **not** accept target selectors.


### Fields

Field | Type | Default | Description
------|------|---------|------------
`name` | **[String]**| | The name of the score holder.
`objective` | **[String]** | | The name of the scoreboard objective.


### Examples

=== "Example #1"

    ``` json
    "score": {
        "name": "aTestScoreHolder",
        "objective": "example"
    }
    ```

    This example will get the score of the `aTestScoreHolder` score holder from the `example` scoreboard objective.


=== "Example #2"

    ``` json
    "score": {
        "name": "#hiddenScoreHolder",
        "objective": "example"
    }
    ```

    This example will get the score of the `#hiddenScoreHolder` score holder from the `example` scoreboard objective.



[Data Type]: ../data_types.md
[String]: https://origins.readthedocs.io/en/latest/types/data_types/string
