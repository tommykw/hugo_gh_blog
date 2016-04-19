+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-04-19T22:58:20+09:00"
menu = "main"
title = "Kotlin any none all"

+++
In this artile describes the colletion function of the stream api of Kotlin.

* any
- Or also applies to conditions in one

```
>>> listOf(1,2,3,4,5).any { it > 4 }
true
>>> listOf(1,2,3,4,5).any { it > 5 }
false
```

* none
- It dose not apply to the conditions

```
>>> listOf(1,2,3,4,5).none { it > 6 }
true
>>> listOf(1,2,3,4,5).none { it > 4 }
false
```

* all
- It applies to all conditions

```
>>> listOf(1,2,3,4,5).all { it > 0 }
true
>>> listOf(1,2,3,4,5).all { it > 4 }
false
```

