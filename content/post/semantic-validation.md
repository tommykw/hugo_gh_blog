+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-11-13T11:54:37+09:00"
menu = "main"
title = "Semantic validation"

+++
Validation of Kotlin function is very useful.
I will explain the semantic validation of Kotlin.

## Argument validaiton
- require

`require` checks arguments.
Seeing the following sources shows you throwing `IllegalArgumentException`

```
@kotlin.internal.InlineOnly
public inline fun require(value: Boolean, lazyMessage: () -> Any): Unit {
    if (!value) {
        val message = lazyMessage()
        throw IllegalArgumentException(message.toString())
    }
}
```

## State validation
- check

`check` checks states.
Seeing the following sources shows you throwing `IllegalStateException`

```
@kotlin.internal.InlineOnly
public inline fun check(value: Boolean, lazyMessage: () -> Any): Unit {
    if (!value) {
        val message = lazyMessage()
        throw IllegalStateException(message.toString())
    }
}
```

## Assertion validation
- assert

An assertion is described as a row and serves as a checkpoint.
If you describe it before any processing you can check the precondition and if it is
later you can check the postcondition.
Runtime assertions have been enabled on the JVM using the `-ea` option.

```
@kotlin.internal.InlineOnly
public inline fun assert(value: Boolean, lazyMessage:() -> Any) {
    @Suppress("NON_PUBLIC_CALL_FROM_PUBLIC_INLINE")
    if (_Assertions.ENABLED) {
        if (!value) {
            val message = lazyMessage()
            throw AssertionError(message)
        }
    }
}
```

require、check and assert are very useful. I will use it in the future.
