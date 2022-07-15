---
title: Meta Action Types
date: 2022-07-13
search:
    boost: 1
---

#   Meta Action Types

Meta action types are independent of the type they operate on, essentially combining or modifying other action types. The actions which are modified have to be of the type the field of the meta action type requires.

For example, if you have a field which requires an **[entity action type]** and you plan to use the **[And (Meta Action Type)]**, the action type provided inside the aforementioned meta action type has to be an **[entity action type]**.

!!! note

    See the documentation for **[Origins/Apoli's meta action types]** for a list of meta action types added by Origins/Apoli.


### List

* [**Loop**](meta_action_types/loop.md)



[entity action type]: entity_action_types.md
[And (Meta Action Type)]: https://origins.readthedocs.io/en/latest/types/meta_action_types/and
[Origins/Apoli's meta action types]: https://origins.readthedocs.io/en/latest/types/meta_action_types
