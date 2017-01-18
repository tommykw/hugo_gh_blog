+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2017-01-19T06:15:57+09:00"
menu = "main"
title = "Platform Types"

+++
Kotlin is nullsafe, but there are things to keep in mind when using Kotlin from Java.
Kotlin has an implementation that accepts it as `T!` Type called Platform types. For example, it is as follows.

```
fun getString(key:String, defValue:String) = sharedPref.getString(key:String, defValue:String) // platform types. return value is T!
fun getString(key:String, defValue:String): String? = sharedPref.getString(key:String, defValue:String) // Declare it to be nullable
```

The above is a simplified method of `SharedPreferences#getString`. but `SharedPreferences#getString` returns @Nullable String.
On the Kotlin side, since it is received as `String:T!`, there is a possibility of crashing at runtime.

By describing it as `@Nullable` on the Java side, platform types and warnings are displayed on the IDE side. in an environment where Kotlin and Java coexist,
it is necessary to understand platform types. Let's explicitly declare whether it is @Nullable in Java.
