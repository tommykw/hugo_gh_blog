+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-03-26T20:02:56+09:00"
menu = "main"
title = "Generic Programming"

+++
Generic Programming is a computer programming method that does not depend on the data format.

# Overview
Generic programming regardless of the fact that either pass or to instantiate the code in the data type,
or the data type as a parameter. You can use the same source code.
This programming is a very powerful, dynamic, highly parameterized software is difficult to understand
than more static software.

# Such as
## Java
Generics has been added in JDK1.5. Generics of Java code to produce only one of the compiled version of the generic class.
Generics Java class can use only the object type as the type parameter.
```
List<Integer> // correct
List<int> // incorrect
```
Generics is to check the correctness of the type at compile time.
Generic type information is removed through a process referred to as a type deletion. 
This is referred to as the erasure type. Only the type information of the parent class is held.

There are several grammar.

- Bounded type parameters

```
class Dog<E extends Animal> {}
```

- Multiple bounds

```
class Foo<E extends A & B & C> {}
```

- Bounded wildcard

```
class Foo(List<? extends Number> list) {}
```

## Haskell
Haskell parameterized type, parametric polymorphism, there is a type class.

## Kotlin

