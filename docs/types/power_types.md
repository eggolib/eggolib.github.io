---
title: Power Types
date: 2022-07-13
search:
    boost: 1
---

#   Power Types

Power types are what grants functionality to powers. Each power has a type, specified with a `type` field in the JSON file. Which type a power is defines which other fields it requires and supports.

Unless stated otherwise, each power type supports a `condition` [**object**][1] field that can check for [**entity condition types**][2]. See [**Power (JSON Format)**][3] for more details.

!!! note

    See the documentation for [**Origins/Apoli's power types**][4] for a list of power types added by Origins/Apoli.


### Regular types

* [**Inventory**](power_types/inventory.md)
* [**Invisibility**](power_types/invisibility.md)
* [**Model Flip**](power_types/model_flip.md)
* [**Starting Equipment**](power_types/starting_equipment.md)


### Action-related

* [**Action on Block Place**](power_types/action_on_block_place.md)
* [**Action on Item Pickup**](power_types/action_on_item_pickup.md)
* [**Action on Key Sequence**](power_types/action_on_key_sequence.md)
* [**Game Event Listener**](power_types/game_event_listener.md)


### Modifying types

* [**Modify Bounciness**](power_types/modify_bounciness.md)
* [**Modify Breathing**](power_types/modify_breathing.md)
* [**Modify Hurt Ticks**](power_types/modify_hurt_ticks.md)
* [**Modify Label Render**](power_types/modify_label_render.md)
* [**Modify Mouse Sensitivity**](power_types/modify_mouse_sensitivity.md)


### Preventing types

* [**Prevent Block Place**](power_types/prevent_block_place.md)
* [**Prevent Critical Hit**](power_types/prevent_critical_hit.md)
* [**Prevent Item Pickup**](power_types/prevent_item_pickup.md)
* [**Prevent Item Use**](power_types/prevent_item_use.md)



[1]: https://origins.readthedocs.io/en/latest/types/data_types/object
[2]: entity_condition_types.md
[3]: https://origins.readthedocs.io/en/latest/json/power
[4]: https://origins.readthedocs.io/en/latest/types/power_types
