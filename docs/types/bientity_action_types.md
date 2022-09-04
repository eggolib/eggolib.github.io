---
title: Bi-entity Action Types
date: 2022-07-29
search:
    boost: 1
---

#   Bi-entity Action Types

Bi-entity action types operate on a `Pair<Entity, Entity>` or in simpler terms: an '**actor**' and a '**target**'. The '**actor**' and the '**target**' is determined by the used power type and can be swapped. These are available to power/action types that provides a `bientity_action` [**object**][1] field.

As a rule of thumb, the '**actor**' is usually the entity that invoked the action *(e.g: uses or attacks an entity)* while the '**target**' is the entity being targeted *(e.g: the entity being used or attacked).*

!!! note

    See the documentation for [**Origins/Apoli's bi-entity action types**][2] for a list of bi-entity action types added by Origins/Apoli.


### List

* [**Damage**](bientity_action_types/damage.md)



[1]: https://origins.readthedocs.io/en/latest/types/data_types/object
[2]: https://origins.readthedocs.io/en/latest/types/bientity_action_types
