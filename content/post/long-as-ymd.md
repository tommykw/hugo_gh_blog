+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-07-30T19:44:16+09:00"
menu = "main"
title = "Long as ymd"

+++
I seconds from the time, minute, I tried to calculate the time in Kotlin.

```
fun longAsYmd(Long time): Unit {
    val t = time.toInt()
    val second = t % 60
    val minutes = t / 60 % 60
    val hour = t / 60 / 60
}
```
