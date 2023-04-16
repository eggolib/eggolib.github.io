---
title: Exposed to Weather (Entity Condition Type)
date: 2023-04-16
search:
    boost: 2
---

#   Exposed to Weather

[**Entity Condition Type**][1]

Checks if the entity is exposed to the sky and certain weather.

Type ID: `eggolib:exposed_to_weather`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`weather` | [**Precipitation**][2] | *optional* | If specified, the condition will check if the entity is exposed to the specified weather.
`thundering` | [**Boolean**][3] | *optional* | If specified, the condition will check if there is a thunderstorm.


### Examples

=== "Example #1"

    ``` json
    "condition": {
        "type": "eggolib:exposed_to_weather",
        "weather": "snow"
    }
    ```

    This example will check if the entity is exposed to the sky and snowy weather.


=== "Example #2"

    ``` json
    "condition": {
        "type": "eggolib:exposed_to_weather",
        "weather": "rain",
        "thundering": true
    }
    ```

    This example will check if the entity is exposed to sky and stormy weather.


[1]: ../entity_condition_types.md
[2]: ../data_types/precipitation.md
[3]: https://origins.readthedocs.io/en/latest/types/data_types/boolean
