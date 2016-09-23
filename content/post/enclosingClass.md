+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-09-23T13:28:04+09:00"
menu = "main"
title = "EnclosingClass"

+++
## What is enclosingClass.

```
https://github.com/MicroUtils/kotlin-logging/blob/5c297178d7edcae6af2e248328c42dad11adc88c/src/main/kotlin/mu/internal/KLoggerNameResolver.kt
inline private fun <T: Any> unwrapCompanionClass(ofClass: Class<T>): Class<*> = 
    if (ofClass.enclosingClass != null && ofClass.enclosingClass.kotlin.companionObject?.java == ofClass) {
        ofClass.enclosingClass
    } else {
        ofClass
    }
```
