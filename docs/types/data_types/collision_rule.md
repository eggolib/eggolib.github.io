---
title: Collision Rule (Data Types)
date: 2023-01-30
search:
    boost: 2
---

#   Collision Rule

[**Data Type**][1]

A [**string**][2] used to determine how collision works in a team.

!!! caution

    Currently, the `pushOtherTeams` and `pushOwnTeam` collision rules have the opposite effect due to [MC-87984](https://bugs.mojang.com/browse/MC-87984).


### Values

Value | Description
------|------------
`always` | The default behavior.
`never` | No entities can push entities in the team.
`pushOtherTeams` | Only entities from another team can push the entities in the team.
`pushOwnTeam` | Only entities in the team can push each other.



[1]: ../data_types.md
[2]: https://origins.readthedocs.io/en/latest/types/data_types/string
