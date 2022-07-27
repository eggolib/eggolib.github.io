---
title: Power Types
date: 2022-07-13
search:
    boost: 1
---

#   Power Types

Power types are what grants functionality to powers. Each power has a type, specified with a `type` field in the JSON file. Which type a power is defines which other fields it requires and supports.

Unless stated otherwise, each power type supports a `condition` **[object]** field that can check for **[entity condition types]**. See **[Power (JSON Format)]** for more details.

!!! note

    See the documentation for **[Origins/Apoli's power types]** for a list of power types added by Origins/Apoli.


### Regular types

* [**Inventory**](power_types/inventory.md)
* [**Invisibility**](power_types/invisibility.md)
* [**Model Flip**](power_types/model_flip.md)


### Action-related

* [**Action on Block Place**](power_types/action_on_block_place.md)


### Modifying types

* [**Modify Hurt Ticks**](power_types/modify_hurt_ticks.md)


### Preventing types

* [**Prevent Block Place**](power_types/prevent_block_place.md)



[object]: https://origins.readthedocs.io/en/latest/types/data_types/object
[entity condition types]: https://origins.readthedocs.io/en/latest/types/entity_condition_types
[Power (JSON Format)]: https://origins.readthedocs.io/en/latest/json/power
[Origins/Apoli's power types]: https://origins.readthedocs.io/en/latest/types/power_types
