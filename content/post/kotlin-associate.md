+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-04-25T16:20:36+09:00"
menu = "main"
title = "Kotlin associate"

+++
According to the kotlin document, you can see that you have to
implement that return Map.
```
inline fun <T, K, V> Sequence<T>.associate(
    transform: (T) -> Pair<K, V>
): Map<K, V>
```

It can be used as follows.
```
>>> listOf(1,2,3,4,5).associate { it to it * 2}
{1=2, 2=4, 3=6, 4=8, 5=10}
```
