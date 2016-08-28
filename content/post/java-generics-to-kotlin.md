+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-08-28T23:01:04+09:00"
menu = "main"
title = "Java generics to kotlin"

+++
Generics code of java was expressed using the reified of kotlin.

```
# Java
public <T extends BaseCode> T getCode(Class<T> type) {
    return (T) codes.get(type);
}
```

```
# Kotlin
inline fun <reified T : BaseCode> Code.system() = getCode(T::class.java)
```
