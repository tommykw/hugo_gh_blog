+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-03-25T15:15:29+09:00"
menu = "main"
title = "Extension And Infix"

+++
I wrote a sample of the extension and the infix in Kotlin. 
What is the infix. Infix ia a infix notation and You can use the infix notation.

Extension
```
>>> fun Int.sameAge(a:Int): Boolean { return this == a }
>>> 10.sameAge(10)
true
>>> 10.sameAge(12)
false
```

Infix and Extension
```
>>> infix fun Int.sameAge(a:Int): Boolean { return this == a}
>>> 10 sameAge 10
true
>>> 10 sameAge 12
false
```

