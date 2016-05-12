+++
Categories = ["Development", "GoLang"]
Description = ""
Tags = ["Development", "golang"]
date = "2016-05-13T05:37:46+09:00"
menu = "main"
title = "Lateinit property before it has been initialized"

+++
The follwing exceptions and are using the lateinit occurred.

```
class UdonMaker {
    lateinit var callback:Callback
    fun onCreate(callback: Callback) {
        this.callback = callback
        ...
    }

    fun onResult(result:Result) {
        if (result.code == "OK") {
            callback.onSucess() // lateinit property before it has been initialized
        } else {
            callback.onFail()
        }
    }

    interface callback {
        onSuccess()
        onFail()
    }
}

fun onCreate() {
    UdonMaker().onCreate(object : Callback {
        override fun onSucess() {}
        override fun onFail() {}
    })
}
```

Accessing a lateinit property before it has been initialized throws a special exception that
clearly identifies the property being accessed and the fact that it hasn't been initialized

```
var callback:Callback? = null
```

