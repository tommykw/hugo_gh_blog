+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-05-08T14:11:37+09:00"
menu = "main"
title = "What is the different singleOrNull and find"

+++
Although I believe that singleOrNull and find proviedes the same function was different.

```
>> listOf(1,2,3).singleOrNull { it > 0 }
null
>>> listOf(1,2,3).find { it > 0 }
1
```

The following is the same result
```
>>> listOf(1,2,3).singleOrNull { it == 1 }
1
>>> listOf(1,2,3).find { it == 1 }
1
```
