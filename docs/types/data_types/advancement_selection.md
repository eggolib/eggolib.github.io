---
title: Advancement Selection
date: 2023-07-06
search:
    boost: 2
---

#   Advancement Selection

[**Data Type**][1]

A string used to determine how the parent(s) and/or child(ren) of an advancement (or advancements in general) is selected.


!!! note

    See [**Minecraft Fandom Wiki: /advancement (Syntax)**][2] for further details on the selection values.


### Values

Value | Description
------|------------
`only` | Grant/revoke only the specified advancement. (or criterion/criteria, if specified)
`from` | Grant/revoke the specified advancement and its children. (e.g: advancement --> child --> child's child --> ...)
`through` | Grant/revoke the parent(s) and child(ren) of the specified advancement. (e.g: parent --> parent's parent --> ... --> root --> specified advancement --> child --> child's child --> ...)
`until` | Grant/revoke the parent(s) of the specified advancement. (e.g: parent --> parent's parent --> ... --> root --> specified advancement)
`everything` | Grant/revoke all advancements.



[1]: ../data_types.md
[2]: https://minecraft.fandom.com/wiki/Commands/advancement#Syntax
