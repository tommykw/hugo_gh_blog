+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-03-16T04:06:54+09:00"
menu = "main"
title = "Way to get the method for java compat"

+++

There is a way to get the method for java compat to become boolean name or getter name
```
var bar: Int = 1
    @JvmName("getBar") get
```

On a data class case
```
data class Bar(@get:JvmName("isBar") val bar: Boolean)
```
