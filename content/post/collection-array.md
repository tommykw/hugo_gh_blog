+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-06-12T11:21:03+09:00"
menu = "main"
title = "Collection array"

+++
There are four of tye array type in Kotlin.

- List
- ArrayList
- Array
- IntArray (In the case of Int)

Kotlin List
```
>>> val a:List<Int> = listOf(1,2,3)
>>> a.add(1)
error: unresolved reference: add

>>> a.javaClass
class java.util.Arrays$ArrayList
```

Kotlin ArrayList
```
// kotlin
>>> val a:ArrayList<Int> = arrayListOf(1,2,3)
error: unresolved reference: ArrayList
val a:ArrayList<Int> = arrayListOf(1,2,3)

>>> val a = arrayListOf(1,2,3)
>>> a.add(1)
true
>>> a.javaClass
class java.util.ArrayList
```
Not work. Because ArrayList is java.util.ArrayList

Kotlin Array
```
>>> val a:Array<Int> = arrayOf(1,2,3)
>>> a.add(1)
error: unresolved reference: add

>>> a.javaClass
class [Ljava.lang.Integer;
```

Kotlin IntArray
```
>>> val a:IntArray = intArrayOf(1,2,3)
>>> a.add(2)
error: unresolved reference: add
a.add(2)

>>> a.javaClass
class [I
```
