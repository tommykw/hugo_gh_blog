+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-03-25T15:06:18+09:00"
menu = "main"
title = "A comma separated"

+++
Attempt to a comma-separated in Kotlin.
There are several patterns. It can be written more concisely than Java.

On kotlinc-jvm
fold method
```
>>> val list = listOf(1,2,3,4,5)
>>> list.fold(StringBuilder()) { builder, i -> builder.append("${i},") }.substring(0, list.size * 2 - 1)
1,2,3,4,5
```

Work in progress: kotlin-stdlib buildString
```
>> buildString { append(list) }
[1, 2, 3, 4, 5]
```
