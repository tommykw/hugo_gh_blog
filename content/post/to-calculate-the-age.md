+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-07-13T21:17:33+09:00"
menu = "main"
title = "To calculate the age"

+++
I want to calculate the age from birthday.
I used the following libraries.

- https://github.com/JakeWharton/ThreeTenABP
 - JSR-310 backport for Android 

```
val age = Period.between(LocalDate.of(1990, 1, 1), LocalDate.now())
age.years // 25
```
