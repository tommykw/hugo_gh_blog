+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-10-01T02:42:06+09:00"
menu = "main"
title = "Nothing"

+++
## stdlib / kotlin / Nothing

```
kotlin/core/builtins/native/kotlin/Nothing.kt

public class Nothing private() {}
```
Nothing has no instances. You can use Nothing to represent "a value that never exists".
for example. if a function has the return type of Nothing. it means that it never returns.

## How to use

When you represent a null is should I use Nothing.

```
>>> fun crash(x:Nothing) {}
>>> crash("foo")
error: type mismatch: inferred type is String but Nothing was expected

>>> fun crash(x:Nothing?) {}
>>> crash(null)
```
