---
title: Class Data Registries
date: 2022-07-14
---

#   Class Data Registries

Class data registries are objects that are instances of `HashMap<String, Class<?>>`, meaning that it's a table of key-value pairs where strings are the keys while Java classes are the values for the keys. It can be used to map the string into a Java class using the [**`ClassDataRegistry#mapStringToClass`**][1] method.


### List

* [**In-Game Screen Class**](class_data_registries/in-game_screen_class.md)



[1]: https://github.com/apace100/calio/blob/master/src/main/java/io/github/apace100/calio/data/ClassDataRegistry.java#L49
