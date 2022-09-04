---
title: Meta Action Types
date: 2022-07-13
search:
    boost: 1
---

#   Meta Action Types

Meta action types are independent of the type they operate on, essentially combining or modifying other action types. The actions which are modified have to be of the type the field of the meta action type requires.

For example, if you have a field which requires an [**entity action type**][1] and you plan to use the [**And (Meta Action Type)**][2], the action type provided inside the aforementioned meta action type has to be an [**entity action type**][1].

!!! note

    See the documentation for [**Origins/Apoli's meta action types**][3] for a list of meta action types added by Origins/Apoli.


### List

* [**Loop**](meta_action_types/loop.md)



[1]: entity_action_types.md
[2]: https://origins.readthedocs.io/en/latest/types/meta_action_types/and
[3]: https://origins.readthedocs.io/en/latest/types/meta_action_types
