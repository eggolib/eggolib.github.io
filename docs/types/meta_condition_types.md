---
title: Meta Condition Types
date: 2022-07-29
search:
    boost: 1
---

#   Meta Condition Types

Meta condition types are independent of the type they operate on, essentially combining or modifying other condition types. The conditions which are modified have to be of the type the field of the meta condition type requires.

For example, if you have a field that requires an [**entity condition type**][1] and you plan to use the [**And (Meta Condition Type)**][2], the condition type provided inside the aforementioned meta condition type has to be an [**entity condition type**][1].

!!! note

    See the documentation for [**Origins/Apoli's meta condition types**][3] for a list of meta condition types added by Origins/Apoli.


### List

* [**Chance**](meta_condition_types/chance.md)



[1]: entity_condition_types.md
[2]: https://origins.readthedocs.io/en/latest/types/entity_condition_types/and
[3]: https://origins.readthedocs.io/en/latest/types/entity_condition_types
